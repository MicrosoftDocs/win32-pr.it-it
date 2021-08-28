---
title: Windows Defender Funzioni
description: Funzioni chiamate dalle app per richiedere analisi, aggiornamenti della firma o informazioni Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483127"
---
# <a name="windows-defender-functions"></a>Windows Defender Funzioni

Funzioni chiamate dalle app per richiedere analisi, aggiornamenti della firma o informazioni Windows Defender.




| Funzione | Descrizione | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | Restituisce un messaggio di errore formattato in base a un codice di errore.<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | Libera memoria per Malware Protection Manager.<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | Chiude l'handle restituito da <a href="mpmanageropen.md"><strong>MpManagerOpen,</strong></a> <a href="mpscanstart.md"><strong>MpScanStart,</strong></a> <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart.</strong></a><br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a> | Stabilisce una connessione a Malware Protection Manager nel computer locale.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>Non supportato.</strong> Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | Restituisce informazioni sulla versione relative ai vari componenti di Malware Protection Manager.<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | Consente il controllo di un'analisi avviata in modo asincrono tramite <a href="mpscanstart.md"><strong>MpScanStart.</strong></a><br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | Avvia un'operazione di analisi.<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | Restituisce un handle di enumerazione allo scopo di recuperare le minacce. Questa funzione può essere usata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione delle minacce o tutte le minacce presenti nel database della firma.<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | Consente di eseguire query su informazioni statiche (ad esempio gravità e categoria) o localizzate (ad esempio descrizione della categoria e consigli) su una determinata minaccia.<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite <a href="mpupdatestart.md"><strong>MpUpdateStart.</strong></a><br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | Avvia un'operazione di aggiornamento della firma.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | Imposta Windows Defender stato su On o Off.<br /><blockquote>[!Note]<br />A partire Windows 10, versione 1607 e Windows Server 2016, la funzione <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> restituisce <strong>sempre E_NOTIMPL</strong>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | Restituisce lo stato corrente di Windows Defender.<br /> | 




 

 

 





