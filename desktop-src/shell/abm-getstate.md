---
description: Recupera gli Stati di Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.
title: Messaggio ABM_GETSTATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342871"
---
# <a name="abm_getstate-message"></a>Messaggio di stato di ABM \_

Recupera gli Stati di Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Quando si invia questo messaggio, è necessario specificare il membro **cbSize** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se la barra delle applicazioni non è né nello stato Nascondi automaticamente né sempre in primo piano. In caso contrario, il valore restituito è uno o entrambi gli elementi seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>La barra delle applicazioni si trova nello stato always on-top. <br/>
<blockquote>
[!Note]<br />
A partire da Windows 7, ABS_ALWAYSONTOP non viene più restituito perché la barra delle applicazioni è sempre in tale stato. Il codice precedente deve essere aggiornato per ignorare l'assenza di questo valore in non presupporre che il valore restituito significhi che la barra delle applicazioni non sia nello stato always on-top.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>La barra delle applicazioni si trova nello stato Nascondi automaticamente.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




