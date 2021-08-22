---
title: CBEM_SETWINDOWTHEME messaggio (Commctrl.h)
description: Imposta lo stile di visualizzazione di un controllo ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- CBEM_SETWINDOWTHEME di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e020c2bb73b2a2a58ee11916f589fb8b5bc1bf9268696f9ff3920ce99248aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527891"
---
# <a name="cbem_setwindowtheme-message"></a>Messaggio CBEM \_ SETWINDOWTHEME

Imposta lo stile di visualizzazione di un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa Unicode che contiene lo stile di visualizzazione del controllo da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32 versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





