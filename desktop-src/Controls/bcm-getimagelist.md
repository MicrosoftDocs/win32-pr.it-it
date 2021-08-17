---
title: BCM_GETIMAGELIST messaggio (Commctrl.h)
description: Ottiene la struttura BUTTON \_ IMAGELIST che descrive l'elenco di immagini assegnato a un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button GetImageList.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST controlli di Windows messaggio
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba74f358e80871ffad4822fd8088ca6aeb58521d8878254ed920356db5a6daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833912"
---
# <a name="bcm_getimagelist-message"></a>Messaggio BCM \_ GETIMAGELIST

Ottiene la [**struttura BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che descrive l'elenco di immagini assegnato a un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)

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

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





