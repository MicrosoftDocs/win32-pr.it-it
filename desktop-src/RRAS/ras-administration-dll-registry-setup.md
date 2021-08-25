---
title: Informazioni sull'installazione del Registro di sistema della DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS. RAS supporta più DLL di amministrazione RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Amministrazione RAS RRAS, configurazione del registro DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dbabc7a667455bce2cffbd3d04591076f820efa755c0f512f27130a82fde4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909911"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Informazioni sull'installazione del Registro di sistema della DLL di amministrazione RAS

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



 

Poiché RAS supporta più DLL di amministrazione RAS, il valore del Registro di sistema **DLLPath** può contenere un elenco di percorsi delimitato da punto e virgola. Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata ProElectron, Inc., potrebbe essere la seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName:* **REG \_ SZ** : ProElectron RAS Admin DLL

*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS chiama le DLL nell'ordine in cui sono elencate in questo valore del Registro di sistema. Il valore *displayName del Registro di* sistema contiene ancora un solo nome visualizzato.

Il programma di installazione per una DLL di amministrazione RAS deve inoltre fornire funzionalità di rimozione e disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema per la DLL.

**Windows 2000/NT:** RAS supporta una sola DLL di amministrazione RAS, quindi il valore del Registro di sistema **DLLPath** non può contenere un elenco di percorsi delimitato da punto e virgola.

 

 




