---
title: Configurazione del registro di sistema della DLL di amministrazione RAS
description: Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516024"
---
# <a name="ras-administration-dll-registry-setup"></a>Configurazione del registro di sistema della DLL di amministrazione RAS

Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Per registrare la DLL, impostare i valori seguenti in questa chiave.



| Nome del valore    | Dati del valore                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Stringa **reg \_ SZ** che contiene il nome visualizzato descrittivo della dll. |
| *DLLPath*     | Stringa **reg \_ SZ** che contiene il percorso completo della dll.                  |



 

Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **reg \_ SZ** : dll amministratore RAS proelectron

*DllPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema della DLL.

 

 




