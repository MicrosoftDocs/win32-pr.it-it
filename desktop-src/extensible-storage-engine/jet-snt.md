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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225883"
---
# <a name="jet_snt"></a>JET_SNT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Il gruppo [JET_SNT]() di costanti descrive i punti dello stato di avanzamento di un'operazione su cui vengono richieste informazioni in una chiamata alla funzione di callback di [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

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
<p><strong>Server Windows 2000:</strong>  L'operazione è stata avviata. In questo caso, l'ultimo parametro della funzione di callback deve essere un puntatore valido a una struttura <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> che indica il numero totale di unità da eseguire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Il numero di unità completate e il numero di unità ancora da eseguire. Queste informazioni vengono restituite nei membri di una struttura <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>Il completamento di un'operazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>Errore di un'operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>Controllo di recupero di un'operazione.</p>
<div class="alert">

> [!NOTE]
> <P>Questo valore non è applicabile alle versioni del sistema operativo Windows a partire da Windows 8.</P>


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
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
