---
description: Di seguito sono riportate le funzioni della libreria del registro di sistema offline.
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: Funzioni della libreria del registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c36afac0b8f5f0aed17b12a7e0562cce75ea69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401388"
---
# <a name="offline-registry-library-functions"></a>Funzioni della libreria del registro di sistema offline

Di seguito sono riportate le funzioni della libreria del registro di sistema offline.



| Funzione                                       | Descrizione                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**ORCloseHive**](orclosehive.md)             | Chiude l'hive del registro di sistema offline specificato e libera la memoria allocata per l'hive.                                 |
| [**ORCloseKey**](orclosekey.md)               | Chiude un handle per la chiave del registro di sistema specificata in un hive del registro di sistema offline.                                          |
| [**ORCreateHive**](orcreatehive.md)           | Crea un hive del registro di sistema offline che contiene una singola chiave radice vuota.                                             |
| [**ORCreateKey**](orcreatekey.md)             | Crea la chiave del registro di sistema specificata in un hive del registro di sistema offline. Se la chiave esiste già, la funzione la apre.   |
| [**ORDeleteKey**](ordeletekey.md)             | Elimina una sottochiave e i relativi valori da un hive del registro di sistema offline.                                                      |
| [**ORDeleteValue**](ordeletevalue.md)         | Rimuove un valore dalla chiave del registro di sistema specificata in un hive del registro di sistema offline.                                        |
| [**OREnumKey**](orenumkey.md)                 | Enumera le sottochiavi della chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.                              |
| [**OREnumValue**](orenumvalue.md)             | Enumera i valori per la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.                              |
| [**ORGetKeySecurity**](orgetkeysecurity.md)   | Recupera una copia del descrittore di sicurezza che protegge la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. |
| [**ORGetValue**](orgetvalue.md)               | Recupera il tipo e i dati per il valore del registro di sistema specificato in un hive del registro di sistema offline.                           |
| [**ORGetVersion**](orgetversion.md)           | Recupera la versione della libreria del registro di sistema offline.                                                              |
| [**ORGetVirtualFlags**](orgetvirtualflags.md) | Recupera i flag virtuali nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.                         |
| [**OROpenHive**](oropenhive.md)               | Carica il file hive specificato in memoria e convalida l'hive.                                                   |
| [**OROpenKey**](oropenkey.md)                 | Apre la chiave del registro di sistema specificata in un hive del registro di sistema offline.                                                       |
| [**ORQueryInfoKey**](orqueryinfokey.md)       | Recupera le informazioni sulla chiave del registro di sistema specificata in un hive del registro di sistema offline.                                 |
| [**ORSaveHive**](orsavehive.md)               | Scrive l'hive del registro di sistema offline specificato in un file.                                                               |
| [**ORSetKeySecurity**](orsetkeysecurity.md)   | Imposta la sicurezza di una chiave del registro di sistema aperta in un hive del registro di sistema offline.                                              |
| [**ORSetValue**](orsetvalue.md)               | Imposta i dati per il valore di una chiave del registro di sistema specificata in un hive del registro di sistema offline.                                |
| [**ORSetVirtualFlags**](orsetvirtualflags.md) | Imposta i flag di virtualizzazione nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.                           |



 

 

 



