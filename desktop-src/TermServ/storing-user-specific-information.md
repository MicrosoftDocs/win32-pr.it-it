---
title: Archiviazione di informazioni specifiche dell'utente
description: Le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente da informazioni globali che si applicano a tutti gli utenti.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aa8e60ec89c3f9d161941d01e1aa241f0bb0245d0f5b57b1cc362dd836bdb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000431"
---
# <a name="storing-user-specific-information"></a>Archiviazione di informazioni specifiche dell'utente

In un Servizi Desktop remoto, le applicazioni devono archiviare le informazioni specifiche dell'utente in posizioni specifiche dell'utente, separatamente dalle informazioni globali applicabili a tutti gli utenti. Questa regola si applica alle informazioni archiviate nel Registro di sistema, nonché alle informazioni archiviate nei file. In generale, non presupporre che un computer sia equivalente a un utente.

Archiviare le informazioni del Registro di sistema specifiche dell'utente nella **chiave del Registro di sistema HKEY \_ CURRENT \_** USER. Servizi Desktop remoto l'hive del Registro di sistema personale dell'utente corrente in **HKEY \_ CURRENT \_ USER** quando l'utente esegue l'accesso. Naturalmente, Servizi Desktop remoto il Registro di sistema per garantire che ognuno dei client connessi rilevi l'hive utente corretto in **HKEY \_ CURRENT \_ USER**. Per altre informazioni sulle chiavi del Registro di sistema, vedere [Sicurezza e](/windows/desktop/SysInfo/registry-key-security-and-access-rights) diritti di accesso delle chiavi del Registro di sistema e [Hive del Registro di sistema.](/windows/desktop/SysInfo/registry-hives)

Al contrario, tutti gli utenti condividono **l'hive \_ HKEY LOCAL \_ MACHINE.** Usare **HKEY \_ LOCAL MACHINE \_ per** archiviare informazioni specifiche del computer, non informazioni specifiche dell'utente.

Archiviare i file delle preferenze utente o altri file specifici dell'utente nella directory radice dell'utente o in una directory specificata dall'utente. Questa considerazione si applica ai file temporanei usati per archiviare informazioni provvisorie (ad esempio i dati memorizzati nella cache) o per passare dati a un'altra applicazione. Anche i file temporanei specifici dell'utente devono essere archiviati per singolo utente.

È possibile usare la [**funzione SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) con il flag CSIDL PERSONAL per ottenere il percorso della directory dei file \_ personali dell'utente. È anche possibile usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per recuperare il percorso della directory Windows directory. In un Servizi Desktop remoto, la directory Windows è garantita come privata per ogni utente. Non archiviare i file specifici dell'utente nella directory di sistema, ad esempio WINDOWS, o nella directory del programma, ad esempio Programmi.

Per evitare conflitti tra le informazioni e le preferenze degli utenti, le applicazioni devono archiviare le informazioni temporanee per utente in file temporanei specifici dell'utente. I file temporanei specifici dell'utente impediscono anche gli errori dell'applicazione causati da conflitti di blocco dei file. Per specificare il percorso per l'archiviazione delle informazioni temporanee, usare [**la funzione GetTempPath.**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha)

 

 