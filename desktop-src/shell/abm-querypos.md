---
description: Richiede una dimensione e una posizione dello schermo per un AppBar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Messaggio ABM_QUERYPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342866"
---
# <a name="abm_querypos-message"></a>\_Messaggio QUERYPOS ABM

Richiede una dimensione e una posizione dello schermo per un AppBar. Quando viene effettuata la richiesta, il messaggio propone un bordo dello schermo e un rettangolo di delimitazione per AppBar. Il sistema regola il rettangolo di delimitazione in modo che AppBar non interferisca con la barra delle applicazioni di Windows o con altre AppBar.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Il membro **uEdge** specifica un bordo dello schermo e il membro **RC** contiene il rettangolo di delimitazione proposto. Quando la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) restituisce, **RC** contiene il rettangolo di delimitazione approvato. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Un AppBar deve inviare questo messaggio prima di inviare il messaggio di [**\_ SETPOS ABM**](abm-setpos.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




