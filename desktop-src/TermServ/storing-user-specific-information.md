---
title: Archiviazione di informazioni specifiche dell'utente
description: Le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente da informazioni globali che si applicano a tutti gli utenti.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046908"
---
# <a name="storing-user-specific-information"></a>Archiviazione di informazioni specifiche dell'utente

In un ambiente di Servizi Desktop remoto, le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente dalle informazioni globali che si applicano a tutti gli utenti. Questa regola si applica alle informazioni archiviate nel registro di sistema e alle informazioni archiviate nei file. In generale, non presupporre che un computer sia equivalente a un utente.

Archiviare le informazioni del registro di sistema specifiche dell'utente nella chiave del registro di sistema **\_ \_ dell'utente corrente di HKEY** . Servizi Desktop remoto carica l'hive del registro di sistema personale dell'utente corrente nell' **\_ \_ utente corrente di HKEY** quando l'utente esegue l'accesso. Naturalmente, Servizi Desktop remoto gestisce il registro di sistema per garantire che ognuno dei client connessi rilevi l'hive utente corretto in **HKEY \_ Current \_ User**. Per ulteriori informazioni sulle chiavi del registro di sistema, vedere [chiave del registro di sistema e diritti di accesso](/windows/desktop/SysInfo/registry-key-security-and-access-rights) e [hive del registro](/windows/desktop/SysInfo/registry-hives)di sistema.

Al contrario, tutti gli utenti condividono l'hive **\_ locale del \_ computer HKEY** . Usare il computer **\_ locale \_ HKEY** per archiviare le informazioni specifiche del computer, non le informazioni specifiche dell'utente.

Archiviare i file preferenza utente o altri file specifici dell'utente nella directory radice dell'utente o in una directory specificata dall'utente. Questa considerazione si applica ai file temporanei utilizzati per archiviare le informazioni provvisorie, ad esempio i dati memorizzati nella cache, o per passare i dati a un'altra applicazione. I file temporanei specifici dell'utente devono essere archiviati anche in base ai singoli utenti.

[](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) \_ Per ottenere il percorso della directory dei file personali dell'utente, è possibile usare la funzione SHGetSpecialFolderLocation con il flag CSIDL Personal. È anche possibile usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per recuperare il percorso della directory di Windows. In un ambiente Servizi Desktop remoto la directory di Windows è garantita come privata per ogni utente. Non archiviare i file specifici dell'utente nella directory di sistema, ad esempio WINDOWS, o directory del programma, ad esempio i file di programma.

Per evitare conflitti tra le informazioni e le preferenze degli utenti, le applicazioni devono archiviare informazioni temporanee per singolo utente in file temporanei specifici dell'utente. Anche i file temporanei specifici dell'utente impediscono gli errori delle applicazioni causati da conflitti di blocco del file. Per specificare il percorso per l'archiviazione di informazioni temporanee, utilizzare la funzione [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) .

 

 