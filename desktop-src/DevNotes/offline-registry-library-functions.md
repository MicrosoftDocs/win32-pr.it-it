---
description: Di seguito sono riportate le funzioni della libreria del Registro di sistema offline.
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: Funzioni della libreria del Registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400aeddf652948fac135b73b0512d157d17b1d71e83b5a5399c5c34618872323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826709"
---
# <a name="offline-registry-library-functions"></a>Funzioni della libreria del Registro di sistema offline

Di seguito sono riportate le funzioni della libreria del Registro di sistema offline.



| Funzione                                       | Descrizione                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**ORCloseHive**](orclosehive.md)             | Chiude l'hive del Registro di sistema offline specificato e libera la memoria allocata per l'hive.                                 |
| [**ORCloseKey**](orclosekey.md)               | Chiude un handle per la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.                                          |
| [**ORCreateHive**](orcreatehive.md)           | Crea un hive del Registro di sistema offline che contiene una singola chiave radice vuota.                                             |
| [**ORCreateKey**](orcreatekey.md)             | Crea la chiave del Registro di sistema specificata in un hive del Registro di sistema offline. Se la chiave esiste già, la funzione la apre.   |
| [**ORDeleteKey**](ordeletekey.md)             | Elimina una sottochiave e i relativi valori da un hive del Registro di sistema offline.                                                      |
| [**ORDeleteValue**](ordeletevalue.md)         | Rimuove un valore dalla chiave del Registro di sistema specificata in un hive del Registro di sistema offline.                                        |
| [**OREnumKey**](orenumkey.md)                 | Enumera le sottochiavi della chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.                              |
| [**OREnumValue**](orenumvalue.md)             | Enumera i valori per la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.                              |
| [**ORGetKeySecurity**](orgetkeysecurity.md)   | Recupera una copia del descrittore di sicurezza che protegge la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline. |
| [**ORGetValue**](orgetvalue.md)               | Recupera il tipo e i dati per il valore del Registro di sistema specificato in un hive del Registro di sistema offline.                           |
| [**ORGetVersion**](orgetversion.md)           | Recupera la versione della libreria del Registro di sistema offline.                                                              |
| [**ORGetVirtualFlags**](orgetvirtualflags.md) | Recupera i flag virtuali sulla chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.                         |
| [**OROpenHive**](oropenhive.md)               | Carica il file hive specificato in memoria e convalida l'hive.                                                   |
| [**OROpenKey**](oropenkey.md)                 | Apre la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.                                                       |
| [**ORQueryInfoKey**](orqueryinfokey.md)       | Recupera informazioni sulla chiave del Registro di sistema specificata in un hive del Registro di sistema offline.                                 |
| [**ORSaveHive**](orsavehive.md)               | Scrive l'hive del Registro di sistema offline specificato in un file.                                                               |
| [**ORSetKeySecurity**](orsetkeysecurity.md)   | Imposta la sicurezza di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.                                              |
| [**ORSetValue**](orsetvalue.md)               | Imposta i dati per il valore di una chiave del Registro di sistema specificata in un hive del Registro di sistema offline.                                |
| [**ORSetVirtualFlags**](orsetvirtualflags.md) | Imposta i flag di virtualizzazione sulla chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.                           |



 

 

 



