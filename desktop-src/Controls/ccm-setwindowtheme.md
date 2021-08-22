---
title: CCM_SETWINDOWTHEME messaggio (Commctrl.h)
description: Imposta lo stile di visualizzazione di un controllo .
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4656290a861247dc474e46cb396314f762f0084f45ae60d32198aa7bb464f8d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320051"
---
# <a name="ccm_setwindowtheme-message"></a>Messaggio \_ CCM SETWINDOWTHEME

Imposta lo stile di visualizzazione di un controllo .

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
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





