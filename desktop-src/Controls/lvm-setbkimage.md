---
title: Messaggio LVM_SETBKIMAGE (COMmctrl. h)
description: Imposta l'immagine di sfondo in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkImage di ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Controlli di Windows Message LVM_SETBKIMAGE
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
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477566"
---
# <a name="lvm_setbkimage-message"></a>\_Messaggio SETBKIMAGE LVM

Imposta l'immagine di sfondo in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkImage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) che contiene le nuove informazioni sull'immagine di sfondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario. Restituisce zero se il membro **ulFlags** della struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) è **LVBKIF \_ source \_ None**.

## <a name="remarks"></a>Commenti

Poiché il controllo elenco-visualizzazione USA OLE COM per manipolare le immagini di sfondo, l'applicazione chiamante deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) prima di inviare questo messaggio. È consigliabile chiamare una di queste funzioni quando l'applicazione viene inizializzata e chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando l'applicazione viene terminata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETBKIMAGE LVM**](lvm-getbkimage.md)
</dt> </dl>

 

