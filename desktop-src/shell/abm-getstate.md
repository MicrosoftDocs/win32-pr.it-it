---
description: Recupera gli stati di visualizzazione automatica e sempre in primo piano della barra Windows barra delle applicazioni.
title: ABM_GETSTATE messaggio (Shellapi.h)
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
ms.openlocfilehash: b1a3618be793f4728dc6184b50b7a4e0e57c3ffd2c4d2cd8acde17372aa031f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225230"
---
# <a name="abm_getstate-message"></a>Messaggio \_ GETSTATE ABM

Recupera gli stati di visualizzazione automatica e sempre in primo piano della barra Windows barra delle applicazioni.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a [**una struttura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) È necessario specificare il **membro cbSize quando** si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se la barra delle applicazioni non si trova né nello stato di visualizzazione automatica né sempre in primo piano. In caso contrario, il valore restituito è uno o entrambi gli elementi seguenti:



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
<td>La barra delle applicazioni è nello stato sempre in primo piano. <br/>
<blockquote>
[!Note]<br />
A Windows 7, ABS_ALWAYSONTOP non viene più restituito perché la barra delle applicazioni si trova sempre in tale stato. Il codice precedente deve essere aggiornato per ignorare l'assenza di questo valore in non presupporre che il valore restituito per indicare che la barra delle applicazioni non si trova nello stato sempre in primo piano.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>La barra delle applicazioni si trova nello stato di visualizzazione automatica.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




