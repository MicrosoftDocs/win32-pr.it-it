---
title: IMAGELISTSTATEFLAGS (COMmctrl. h)
description: I flag seguenti vengono passati al metodo di IImageList di richiamo nel membro fState di IMAGELISTDRAWPARAMS.
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
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048199"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

I flag seguenti vengono passati al metodo [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) nel membro **fState** di [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Costante/valore                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_**</dt> <dt>0x00000000</dt> normale </dl>       | Lo stato dell'immagine non viene modificato.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_**</dt> <dt>0x00000001</dt> Glow </dl>             | Non supportata. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_**</dt> <dt>0x00000002</dt> Shadow </dl>       | Non supportata. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ SATURA**</dt> <dt>0x00000004</dt> </dl> | Riduce la saturazione del colore dell'icona in scala di grigi. Questa operazione influiscono solo sulle immagini 32bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_**</dt> <dt>0x00000008</dt> alfa </dl>          | Alfa fonde l'icona. La fusione alfa controlla il livello di trasparenza di un'icona, in base al valore del canale alfa. Il valore del canale alfa è indicato dal membro **frame** nel metodo [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) . Il canale alfa può essere compreso tra 0 e 255, mentre 0 è completamente trasparente e 255 è completamente opaco.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

