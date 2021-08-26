---
title: LVM_SETBKIMAGE messaggio (Commctrl.h)
description: Imposta l'immagine di sfondo in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView SetBkImage.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f00fbf02d4e354115c01af637251782adb9f95b11923d12cba4bc9f1a0f9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919971"
---
# <a name="lvm_setbkimage-message"></a>Messaggio LVM \_ SETBKIMAGE

Imposta l'immagine di sfondo in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetBkImage.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) che contiene le nuove informazioni sull'immagine di sfondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Restituisce zero se il **membro ulFlags** della struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) è **LVBKIF \_ SOURCE \_ NONE.**

## <a name="remarks"></a>Commenti

Poiché il controllo visualizzazione elenco usa OLE COM per modificare le immagini di sfondo, l'applicazione chiamante deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) prima di inviare questo messaggio. È meglio chiamare una di queste funzioni quando l'applicazione viene inizializzata e chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando l'applicazione viene terminare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ GETBKIMAGE**](lvm-getbkimage.md)
</dt> </dl>

 

