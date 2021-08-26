---
title: Configurazione del Registro di sistema della DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e40ed8fe4fe853c12e33e6168cb72cf1b3ec5b33afc92e8767731a13ec37412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036366"
---
# <a name="ras-administration-dll-registry-setup"></a>Configurazione del Registro di sistema della DLL di amministrazione RAS

Il programma di installazione per una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni nella chiave seguente nel Registro di sistema.

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
| *DisplayName* | Stringa **REG \_ SZ** che contiene il nome visualizzato descrittivo della DLL. |
| *DLLPath*     | Stringa **REG \_ SZ** che contiene il percorso completo della DLL.                  |



 

Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata ProElectron, Inc. potrebbe essere:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName:* **REG \_ SZ** : ProElectron RAS Admin DLL

*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Il programma di installazione per una DLL di amministrazione RAS deve inoltre fornire funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema della DLL.

 

 




