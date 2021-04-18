---
description: 'Altre informazioni su: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305770"
---
# <a name="jet_snp"></a>JET_SNP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

Il **JET_SNP** gruppo di costanti descrive il tipo di operazione per cui è necessario ottenere informazioni sullo stato di avanzamento. Queste costanti vengono usate come parametro *SNP* della funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

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
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>Il callback è per un'operazione di ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>Il callback è per la deframmentazione del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>Il callback è per un'operazione di ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>Il callback è per un'operazione di backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>Non supportata.</p>
<p><strong>Windows 2000:</strong>  Il callback è per l'operazione di aggiornamento del formato del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>Il callback è per un'operazione di azzeramento del database (ovvero, pulitura).</p>
<p><strong>Windows server 2003 e windows 2000 Server:</strong>  Non supportato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>Il callback è per il processo di aggiornamento del formato di record di tutte le pagine del database.</p>
<p><strong>Windows server 2003 e windows 2000 Server:</strong>  Non supportato.</p></td>
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
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
