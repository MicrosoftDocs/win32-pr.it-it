---
title: Configurazione del Registro di sistema della DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406714"
---
# <a name="ras-administration-dll-registry-setup"></a>Configurazione del Registro di sistema della DLL di amministrazione RAS

Il programma di installazione per una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo informazioni nella chiave seguente nel Registro di sistema.

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



 

Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS di una società fittizia denominata ProElectron, Inc. potrebbe essere:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **REG \_ SZ** : PROElectron RAS Admin DLL

*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Anche il programma di installazione per una DLL di amministrazione RAS deve fornire funzionalità di rimozione/disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema della DLL.

 

 




