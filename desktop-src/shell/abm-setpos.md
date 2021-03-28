---
description: Imposta la dimensione e la posizione dello schermo di un AppBar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Messaggio ABM_SETPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525428"
---
# <a name="abm_setpos-message"></a>\_Messaggio SETPOS ABM

Imposta la dimensione e la posizione dello schermo di un AppBar. Il messaggio specifica un bordo dello schermo e il rettangolo di delimitazione per AppBar. Il sistema può regolare il rettangolo di delimitazione in modo che AppBar non interferisca con la barra delle applicazioni di Windows o con altre AppBar.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Il membro **uEdge** specifica un bordo dello schermo e il membro **RC** contiene il rettangolo di delimitazione. Quando la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) restituisce, **RC** contiene il rettangolo di delimitazione approvato. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Questo messaggio consente al sistema di inviare il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) a tutti i AppBar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




