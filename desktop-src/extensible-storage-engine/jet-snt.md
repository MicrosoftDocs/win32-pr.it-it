---
description: 'Altre informazioni su: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad04730c52bce38e462c2521dc7c34872bfcb69c3337ac6af18d09d865b9cfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252515"
---
# <a name="jet_snt"></a>JET_SNT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Il [JET_SNT]() di costanti descrive i punti di avanzamento di un'operazione sui quali vengono richieste informazioni in una chiamata alla funzione di [callback](./jet-pfnstatus-callback-function.md) JET_PFNSTATUS di callback.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Costante/valore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_sntBegin<br />
5</p></td>
<td><p>Inizio di un'operazione</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>Non supportata.</p>
<p><strong>Windows 2000 Server:</strong>  L'operazione viene avviata. In questo caso, l'ultimo parametro della funzione di callback deve essere un puntatore valido a una <a href="gg269328(v=exchg.10).md">struttura JET_SNPROG</a> che indica il numero totale di unità da eseguire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Numero di unità completate e numero di unità ancora da eseguire. Queste informazioni vengono restituite nei membri di una <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> struttura .</p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>Completamento di un'operazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>Errore di un'operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>Controllo di ripristino di un'operazione.</p>
<div class="alert">

> [!NOTE]
> <P>Questo valore non è applicabile alle versioni del Windows operativo a partire da Windows 8.</P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
