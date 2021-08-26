---
title: BCM_SETIMAGELIST messaggio (Commctrl.h)
description: Assegna un elenco di immagini a un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button SetImageList.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST controlli di Windows messaggio
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5c88020bb139c358b17386b003bfb9de9cfcd4e769b9262ed90e23f3f95e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921561"
---
# <a name="bcm_setimagelist-message"></a>Messaggio BCM \_ SETIMAGELIST

Assegna un elenco di immagini a un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che contiene informazioni sull'elenco di immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **TRUE.** In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

L'elenco di immagini a cui si fa riferimento nel membro **himl** della struttura [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve contenere una singola immagine da usare per tutti gli stati o singole immagini per ogni stato. Gli stati seguenti sono definiti in vssym32.h.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Si noti che PBS \_ STYLUSHOT viene usato solo nei tablet computer.

Ogni valore è un indice dell'immagine appropriata nell'elenco di immagini. Se è presente una sola immagine, viene usata per tutti gli stati. Se l'elenco di immagini contiene più di un'immagine, ogni indice corrisponde a uno stato del pulsante. Se non viene fornita un'immagine per ogni stato, non viene disegnato nulla per tali stati senza immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





