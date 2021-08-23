---
title: IMAGELISTSTATEFLAGS (Commctrl.h)
description: I flag seguenti vengono passati al metodo Draw IImageList nel membro fState di IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb4eef2f744c78e84999e9f07f3ca5a06d5dbf93dbfa26d5c6593d94d4e19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576141"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

I flag seguenti vengono passati al [**metodo IImageList::D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) nel membro **fState** di [**IMAGELISTDRAWPARAMS.**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)



| Costante/valore                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ Normal**</dt> <dt>0x00000000</dt> </dl>       | Lo stato dell'immagine non viene modificato.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ ALONE**</dt> <dt>0x00000001</dt> </dl>             | Non supportata. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ Shadow**</dt> <dt>0x00000002</dt> </dl>       | Non supportata. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ SATURAZIONE**</dt> <dt>0x00000004</dt> </dl> | Riduce la saturazione dei colori dell'icona alla scala di grigi. Questo influisce solo su immagini 32bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ Valori alfa**</dt> <dt>0x00000008</dt> </dl>          | Alfa sfusa l'icona. La fusione alfa controlla il livello di trasparenza di un'icona, in base al valore del canale alfa. Il valore del canale alfa è indicato dal membro **frame** nel [**metodo IMAGELISTDRAWPARAMS.**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) Il canale alfa può essere da 0 a 255, con 0 completamente trasparente e 255 completamente opaco.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

