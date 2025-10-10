# Descripció de la tasca 3
## Enunciat  

### Recuperació d’accés i fortificació del GRUB — Procediment

Després de la primera feina exitosa, us arriba un encàrrec urgent que obliga a adoptar mesures immediates per donar-li solució.

### Context
Han arribat a la consultora un equip d’un client. Tenen un **portàtil amb Zorin OS** (Linux amb entorn gràfic) que utilitzava un directiu. Aquest directiu **ha oblidat la contrasenya** i és necessari recuperar l’accés perquè hi ha documentació important. Per evitar danyar l’equip original, el disc ha estat **clonat** i us l’han facilitat en **un disc virtual** per a què hi treballeu.

---

### Objectius
1. Crear una màquina virtual i connectar-hi el disc clònic.  
2. Entrar a la màquina virtual, identificar l’usuari existent i assignar-li una contrasenya nova.  
3. Verificar l’accés amb la nova contrasenya.  
4. Investigar i aplicar mesures per **fortificar l’accés al GRUB** perquè no es pugui reiniciar la contrasenya fàcilment.  
5. Documentar tot el procediment (incloent imatges) per pujar-ho al repositori.

---

### Procediment general (resum)
1. **Preparar la VM**
   - Crear una màquina virtual (p. ex. amb VirtualBox / QEMU / VMware).
   - Connectar el disc virtual clònic com a disc de la VM.

2. **Accés i identificació**
   - Arrancar la VM i accedir al GRUB si cal.
   - Accedir a un *shell* de recuperació (rescat mode) per muntar el sistema de fitxers.
   - Identificar el/els usuaris existents del sistema.

3. **Canvi de contrasenya**
   - Recuperar accés a l’arrel del sistema muntat (`chroot` o muntatge + `passwd`).
   - Canviar la contrasenya de l’usuari identificat.
   - Reiniciar i verificar l’accés amb la nova contrasenya.

4. **Fortificació del GRUB**
   - Investigar i aplicar mesures per protegir GRUB amb contrasenya per impedir entrades de recuperació no autoritzades.
   - Configurar el fitxer `/etc/grub.d/00_header` o `/boot/grub/grub.cfg` segons el mètode triat per afegir protecció.

5. **Documentació**
   - Captures d’imatges dels passos rellevants (pantalla del GRUB, comandes usades, resultats).
   - Documentar comandes i configuracions utilitzades.
   - Pujar el document final (amb imatges i explicacions) al repositori corresponent.
  
     ---

  ## Solució

  Teniu la solució en l'arxiu del següent enllaç : [Solució](solucio.md)
  
  [← Tornar a la pàgina del projecte](../README.md)
