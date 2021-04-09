---
title: Informazioni sulla configurazione del registro di sistema della DLL di amministrazione RAS
description: Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Amministrazione RAS RRAS, configurazione del registro di sistema DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857826"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Informazioni sulla configurazione del registro di sistema della DLL di amministrazione RAS

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



 

Poiché RAS supporta più DLL di amministrazione RAS, il valore del registro di sistema **DllPath** può contenere un elenco delimitato da punti e virgola di percorsi. Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere la seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : dll amministratore RAS proelectron

*DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll

RAS chiama le dll nell'ordine in cui sono elencate in questo valore del registro di sistema. Il valore del registro di sistema *DisplayName* contiene ancora un solo nome visualizzato.

Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione e disinstallazione. Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema per la DLL.

**Windows 2000/NT:** RAS supporta solo una DLL di amministrazione RAS, quindi il valore del registro di sistema **DllPath** non può contenere un elenco delimitato da punti e virgola di percorsi.

 

 




