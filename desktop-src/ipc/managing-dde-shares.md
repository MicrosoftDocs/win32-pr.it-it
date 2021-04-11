---
description: DDE di rete fornisce funzioni che consentono di eliminare una condivisione, ottenere o impostare le informazioni di condivisione o enumerare le condivisioni.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gestione delle condivisioni DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350951"
---
# <a name="managing-dde-shares"></a>Gestione delle condivisioni DDE

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

DDE di rete fornisce funzioni che consentono di eliminare una condivisione, ottenere o impostare le informazioni di condivisione o enumerare le condivisioni.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attività</th>
<th>Procedura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Eliminare una condivisione DDE</td>
<td>Usare la funzione <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</td>
</tr>
<tr class="even">
<td>Ottenere informazioni sulla condivisione DDE</td>
<td>Usare la funzione <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</td>
</tr>
<tr class="odd">
<td>Impostare le informazioni sulla condivisione DDE</td>
<td>Usare la funzione <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td>Enumera condivisioni DDE</td>
<td>Usare la funzione <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> . È inoltre possibile enumerare le condivisioni DDE attendibili tramite la funzione <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>Enumerazione degli utenti connessi</td>
<td>Usare la funzione <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</td>
</tr>
<tr class="even">
<td>Modificare il nome della condivisione DDE</td>
<td>Eliminare la condivisione precedente e creare una nuova condivisione.
<ol>
<li>Recuperare le informazioni sulla condivisione utilizzando <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Rimuovere la condivisione usando <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</li>
<li>Modificare il membro <strong>lpszShareName</strong> della struttura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> restituita da <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Passare la struttura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificata a <a href="nddeshareadd.md"><strong>NDDEShareAdd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

