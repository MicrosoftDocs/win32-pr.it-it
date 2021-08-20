---
description: Windows Update Agent (WUA) si aggiorna automaticamente quando è connesso a un server Windows Server Update Services (WSUS) o a Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Aggiornamento Windows'agente di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388475aaf9fa83413a916520035eb9539187390bf5a3bd8f5c836cb1b176357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814652"
---
# <a name="updating-windows-update-agent"></a>Aggiornamento Windows'agente di aggiornamento

Windows Update Agent (WUA) si aggiorna in vari modi, a seconda della versione di Windows in esecuzione nel dispositivo. Le versioni precedenti di WUA potrebbero non essere in grado di connettersi ai servizi di aggiornamento correnti, potrebbero non essere compatibili con tutti gli aggiornamenti e potrebbero non supportare tutte le API documentate. Ecco come assicurare che WUA sia completamente aggiornato e compatibile.

**Nelle versioni di Windows a partire da Windows 7 e Windows Server 2008 R2**

Windows Gli aggiornamenti dell'agente di aggiornamento (WUA) sono inclusi negli aggiornamenti periodici regolari Windows distribuiti tramite Windows Update o Windows Server Update Services (WSUS). Non è necessario eseguire passaggi speciali per aggiornare WUA in queste Windows versioni.

**Nelle versioni di Windows precedenti Windows 7 e Windows Server 2008 R2**

WUA si aggiorna automaticamente quando Aggiornamenti automatici si connette a Windows Update o a WSUS.

Se Aggiornamenti automatici non è ancora stato eseguito correttamente, è possibile che in un dispositivo che esegue queste versioni di Windows sia in esecuzione una versione precedente di WUA che non supporta tutte le API documentate. Se si riceve un risultato WU_E_SELFUPDATE_REQUIRED quando si usa l'API WUA per eseguire un'analisi, un download o un'installazione, questo errore indica che la versione installata di WUA è troppo vecchia per connettersi ai servizi Windows Update correnti. Non è possibile usare le NORMALI API WUA per aggiornare WUA in questi sistemi operativi. 

Un utente può aggiornare manualmente WUA a una versione corrente aprendo il pannello di controllo Windows Update, selezionando Controlla aggiornamenti e quindi accettando l'aggiornamento automatico visualizzato. In alternativa, è possibile aggiornare WUA a livello di codice.

**Per aggiornare WUA a livello di codice nelle versioni di Windows precedenti a Windows 7 e Windows Server 2008 R2**

1.  Usare le [API WinHTTP](../winhttp/winhttp-start-page.md) per [ scaricare ](https://update.microsoft.com/redist/wuredist.cab)Wuredist.cab.
2.  Usare Le [funzioni di crittografia](../seccrypto/cryptography-functions.md) per verificare che la copia scaricataWuredist.cabuna firma digitale da Microsoft. [](https://update.microsoft.com/redist/wuredist.cab) Se non è possibile verificare la firma digitale, arrestarla.
3.  Usare le [API dell'interfaccia di decompressione](../devnotes/cabinet-api-functions.md) file per estrarre il file XML [ daWuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Usare le API Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) per caricare il file XML e individuare il nodo WURedist/StandaloneRedist/architecture per l'architettura del computer. Ad esempio, per x86, individuare il nodo WURedist/StandaloneRedist/architecture con l'attributo **name** di x86.
5.  Chiamare [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) per determinare la versione corrente di WUA. Se **IWindowsUpdateAgentInfo::GetInfo** restituisce un numero di versione almeno alto quanto l'attributo **clientVersion** nel nodo dell'architettura individuato, arrestare.
6.  Usare le [API MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) per leggere **l'attributo downloadUrl** dal nodo dell'architettura che si trova. **downloadUrl** fornisce l'URL di download per il programma di installazione WUA appropriato per l'architettura del computer.
7.  Usare le [API WinHTTP](../winhttp/winhttp-start-page.md) per scaricare il programma di installazione appropriato.
8.  Usare la [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o un'API simile per eseguire il programma di installazione scaricato.

 

 
