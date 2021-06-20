---
title: Informazioni sull'installazione del Registro di sistema delle DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS. RAS supporta più DLL di amministrazione RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Amministrazione RAS RRAS, configurazione del Registro di sistema DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406664"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Informazioni sull'installazione del Registro di sistema delle DLL di amministrazione RAS

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



 

Poiché RAS supporta più DLL di amministrazione RAS, il valore **dllPath** del Registro di sistema può contenere un elenco di percorsi delimitato da punto e virgola. Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS di una società fittizia denominata ProElectron, Inc., potrebbe essere la seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : PROElectron RAS Admin DLL

*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS chiama le DLL nell'ordine in cui sono elencate in questo valore del Registro di sistema. Il valore del Registro di sistema *DisplayName* contiene ancora un solo nome visualizzato.

Anche il programma di installazione per una DLL di amministrazione RAS deve fornire funzionalità di rimozione e disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema per la DLL.

**Windows 2000/NT:** RAS supporta una sola DLL di amministrazione RAS, quindi il valore del Registro di sistema **DLLPath** non può contenere un elenco di percorsi delimitato da punto e virgola.

 

 




