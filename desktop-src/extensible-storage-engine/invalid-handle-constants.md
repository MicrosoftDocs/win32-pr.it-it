---
description: 'Altre informazioni su: costanti handle non valide'
title: Costanti handle non valide
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058160"
---
# <a name="invalid-handle-constants"></a>Costanti handle non valide


_**Si applica a:** Windows | Windows Server_

## <a name="invalid-handle-constants"></a>Costanti handle non valide

Le costanti seguenti indicano handle non validi per diversi aspetti di ESE.

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
<td><p>JET_instanceNil<br />
(~ (JET_INSTANCE) 0)</p></td>
<td><p>Handle non valido per un'istanza di database.<br />
<strong>Windows XP:</strong> Introdotta in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
(~ (JET_SESID) 0)</p></td>
<td><p>Handle non valido per un ID di sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
(~ (JET_TABLEID) 0)</p></td>
<td><p>Handle non valido per un ID tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
((JET_GRBIT) 0)</p></td>
<td><p>Handle non valido per un gruppo di bit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
(~ (JET_LS) 0)</p></td>
<td><p>Handle non valido per l'archiviazione locale.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
((JET_DBID) 0xFFFFFFFF)</p></td>
<td><p>Handle non valido per l'ID del database.</p></td>
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

