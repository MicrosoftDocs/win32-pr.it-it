---
description: Un dispositivo può generare un numero elevato di eventi e ogni evento può essere gestito da uno dei diversi gestori.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Come registrare un gestore eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979522"
---
# <a name="how-to-register-an-event-handler"></a>Come registrare un gestore eventi

Un dispositivo può generare un numero elevato di eventi e ogni evento può essere gestito da uno dei diversi gestori. In Windows XP vengono definiti gli eventi seguenti:

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Istruzioni


I gestori eventi sono definiti sotto la chiave **EventHandlers** . I valori di una chiave del gestore eventi sono i nomi di ogni gestore da cui l'utente deve scegliere quando viene rilevato l'evento. Nessun valore di dati associato a queste voci. Di seguito è riportata una definizione di esempio per un gestore eventi personalizzato denominato **MyNewRemovalEventHandler**, che presenta le possibilità di gestione per l'utente:

-   Gestore da usare se l'evento viene rilevato in un dispositivo creato dalla società denominata Contoso, Inc.
-   Gestore da usare se l'evento viene rilevato in un dispositivo creato dalla società denominata Fabrikam, Inc.
-   Gestore da utilizzare in tutti gli altri casi.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

Dopo aver definito un gestore eventi, è necessario registrarlo con un gestore di dispositivo per una delle possibilità di evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval. MyNewRemovalEventHandler, definito in precedenza, viene usato per DeviceRemoval in un gestore di dispositivo personalizzato denominato MyDeviceHandler e viene definito a tale scopo nell'esempio seguente. Anche in questo caso il valore del registro di sistema non ha alcun componente dati.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

Windows XP predefinisce il seguente set di EventHandlers. 

| Chiave EventHandlers        | Media o tipo di file                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | CD-R/CD-RW vuoti                               |
| ShowPicturesOnArrival    | File immagine                                  |
| PlayMusicFilesOnArrival  | File musicali                                    |
| PlayVideoFilesOnArrival  | File video                                    |
| PlayCDAudioOnArrival     | CD audio (CD di formato REDBOOK con tracce audio) |
| PlayDVDMovieOnArrival    | Film DVD                                     |



 

Windows Vista predefinisce il seguente set di EventHandlers, oltre a quelli descritti in precedenza. 

| Chiave EventHandlers              | Media o tipo di file   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Film di Super VideoCD |
| PlayVideoCDMovieOnArrival      | Film VideoCD       |



 

 

 



