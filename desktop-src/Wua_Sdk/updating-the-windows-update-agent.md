---
description: Windows Update Agent (WUA) si aggiorna automaticamente quando è connesso a un server di Windows Server Update Services (WSUS) o Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Aggiornamento dell'agente di Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fe439b1bea377e2699f6fe5714b208ac5d951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307584"
---
# <a name="updating-windows-update-agent"></a>Aggiornamento dell'agente di Windows Update

Windows Update Agent (WUA) si aggiorna con diversi mezzi, a seconda della versione di Windows in esecuzione sul dispositivo. Le versioni precedenti di WUA potrebbero non essere in grado di connettersi ai servizi di aggiornamento correnti, potrebbero non essere compatibili con tutti gli aggiornamenti e potrebbero non supportare tutte le API documentate. Ecco come verificare che WUA sia completamente aggiornato e compatibile.

**Nelle versioni di Windows a partire da Windows 7 e Windows Server 2008 R2**

Gli aggiornamenti di Windows Update Agent (WUA) sono inclusi negli aggiornamenti periodici regolari di Windows distribuiti tramite Windows Update o per Windows Server Update Services (WSUS). Non è necessario eseguire alcun passaggio speciale per aggiornare WUA in queste versioni di Windows.

**Nelle versioni di Windows precedenti a Windows 7 e Windows Server 2008 R2**

WUA si aggiorna automaticamente quando Aggiornamenti automatici si connette a Windows Update o a WSUS.

Se Aggiornamenti automatici non è ancora stato eseguito correttamente, è possibile che un dispositivo che esegue queste versioni di Windows esegua una versione precedente di WUA che non supporta tutte le API documentate. Se si riceve un risultato WU_E_SELFUPDATE_REQUIRED quando si usa l'API WUA per eseguire un'analisi, scaricare o installare, questo errore indica che la versione installata di WUA è troppo vecchia per connettersi ai servizi Windows Update correnti. Non è possibile usare le normali API WUA per aggiornare WUA in questi sistemi operativi. 

Un utente può aggiornare manualmente WUA a una versione corrente aprendo il pannello di controllo Windows Update, selezionando Controlla aggiornamenti, quindi accettando l'aggiornamento automatico visualizzato. In alternativa, è possibile aggiornare WUA a livello di codice.

**Per aggiornare WUA a livello di codice nelle versioni di Windows precedenti a Windows 7 e Windows Server 2008 R2**

1.  Usare le API [WinHTTP](../winhttp/winhttp-start-page.md) per scaricare [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
2.  Utilizzare le [funzioni di crittografia](../seccrypto/cryptography-functions.md) per verificare che la copia scaricata di [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) disponga di una firma digitale di Microsoft. Se non è possibile verificare la firma digitale, arrestare.
3.  Utilizzare le API dell' [interfaccia di decompressione file](../devnotes/cabinet-api-functions.md) per estrarre il file XML dalla [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Utilizzare le API Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) per caricare il file XML e individuare il nodo WURedist/StandaloneRedist/Architecture per l'architettura del computer. Per x86, ad esempio, individuare il nodo WURedist/StandaloneRedist/Architecture con l'attributo **Name** di x86.
5.  Chiamare [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) per determinare la versione corrente di WUA. Se **IWindowsUpdateAgentInfo:: GetInfo** restituisce un numero di versione che è almeno uguale all'attributo **ClientVersion** nel nodo Architecture individuato, arrestare.
6.  Utilizzare le API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) per leggere l'attributo **DownloadUrl** dal nodo Architecture individuato. **DownloadUrl** fornisce l'URL di download per il programma di installazione di WUA appropriato per l'architettura del computer.
7.  Utilizzare le API [WinHTTP](../winhttp/winhttp-start-page.md) per scaricare il programma di installazione appropriato.
8.  Usare la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o un'API simile per eseguire il programma di installazione scaricato.

 

 
