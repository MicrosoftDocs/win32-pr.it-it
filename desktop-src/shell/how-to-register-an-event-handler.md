---
description: Un dispositivo può generare potenzialmente molti eventi e ogni evento può essere gestito da uno dei diversi gestori.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Come registrare un gestore eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090561"
---
# <a name="how-to-register-an-event-handler"></a>Come registrare un gestore eventi

Un dispositivo può generare potenzialmente molti eventi e ogni evento può essere gestito da uno dei diversi gestori. In Windows XP sono definiti gli eventi seguenti:

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Istruzioni


I gestori eventi sono definiti nella **chiave EventHandlers.** I valori di una chiave del gestore eventi sono i nomi di ogni gestore tra cui l'utente deve scegliere quando viene rilevato l'evento. A queste voci non è associato alcun valore di dati. Di seguito è riportata una definizione di esempio per un gestore eventi personalizzato denominato **MyNewRemovalEventHandler**, che presenta all'utente queste possibilità di gestore:

-   Gestore da utilizzare se l'evento viene rilevato in un dispositivo creato dalla società denominata Contoso, Inc.
-   Gestore da utilizzare se l'evento viene rilevato in un dispositivo creato dalla società denominata Fabrikam, Inc.
-   Gestore da usare in tutti gli altri casi.

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

Dopo aver definito un gestore eventi, è necessario registrarlo con un gestore di dispositivi per una delle possibilità di evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval. MyNewRemovalEventHandler, definito in precedenza, viene usato per DeviceRemoval in un gestore di dispositivo personalizzato denominato MyDeviceHandler ed è definito a tale scopo nell'esempio seguente. Anche in questo caso, il valore del Registro di sistema non include alcun componente dati.

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

Windows XP predefinisce il set di EventHandlers seguente. 

| Tasto EventHandlers        | Supporto o tipo di file                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | CD-R/CD-RW vuoto                               |
| ShowPicturesOnArrival    | File di immagine                                  |
| PlayMusicFilesOnArrival  | Musica file                                    |
| PlayVideoFilesOnArrival  | File video                                    |
| PlayCDAudioOnArrival     | CD audio (CD in formato REDBOOK con tracce audio) |
| PlayDVDMovieOnArrival    | Film DVD                                     |



 

Windows Vista predistina il set seguente di EventHandlers oltre a quelli elencati in precedenza. 

| Tasto EventHandlers              | Supporto o tipo di file   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Film Super VideoCD |
| PlayVideoCDMovieOnArrival      | VideoCD movie       |



 

 

 



