---
title: Funzioni di Windows Defender
description: Funzioni chiamate dalle app per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398496"
---
# <a name="windows-defender-functions"></a>Funzioni di Windows Defender

Funzioni chiamate dalle app per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></td>
<td>Restituisce un messaggio di errore formattato basato su un codice di errore.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></td>
<td>Libera la memoria per malware Protection Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></td>
<td>Chiude l'handle restituito da <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></td>
<td>Stabilisce una connessione a malware Protection Manager nel computer locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></td>
<td><strong>Non supportato.</strong> Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></td>
<td>Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></td>
<td>Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></td>
<td>Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>MpScanStart</strong></a></td>
<td>Avvia un'operazione di analisi.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></td>
<td>Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></td>
<td>Restituisce un handle di enumerazione allo scopo di recuperare le minacce. Questa funzione può essere utilizzata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione da minacce o tutte le minacce presenti nel database di firma.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></td>
<td>Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></td>
<td>Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></td>
<td>Avvia un'operazione di aggiornamento della firma.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></td>
<td>Modifica lo stato di Windows Defender su on o off.<br/>
<blockquote>
[!Note]<br />
A partire da Windows 10, versione 1607 e Windows Server 2016, la funzione <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> restituisce sempre <strong>E_NOTIMPL</strong>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></td>
<td>Restituisce lo stato corrente di Windows Defender.<br/></td>
</tr>
</tbody>
</table>



 

 

 





