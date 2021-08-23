---
title: IMAGELISTDRAWFLAGS (Commctrl.h)
description: Passato al metodo Draw IImageList nel membro fStyle di IMAGELISTDRAWPARAMS.
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44d863e82cf126c62262a564e5bf8366fbe71dbb75cc6d47bd16634d798cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544541"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Passato al [**metodo IImageList::D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) nel membro **fStyle** di [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Costante/valore                                                                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**ILD \_ Normal**</dt> <dt>0x00000000</dt> </dl>                      | Disegna l'immagine usando il colore di sfondo per l'elenco di immagini. Se il colore di sfondo è il valore \_ CLR NONE, l'immagine viene disegnata in modo trasparente usando la maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**ILD \_ TRANSPARENT**</dt> <dt>0x00000001</dt> </dl>       | Disegna l'immagine in modo trasparente usando la maschera, indipendentemente dal colore di sfondo. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**ILD \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Disegna l'immagine, combinando il 25% con il colore di fusione specificato da **rgbFg**. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**ILD \_ FOCUS**</dt> <dt>0x00000002</dt> </dl>                         | Uguale a **ILD \_ BLEND25.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**ILD \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Disegna l'immagine, combinando il 50% con il colore di fusione specificato da **rgbFg**. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**ILD \_ SELECTED**</dt> <dt>0x00000004</dt> </dl>                | Uguale a **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**ILD \_ 0X00000004**</dt> <dt></dt> </dl>                         | Uguale a **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**ILD \_ Maschera**</dt> <dt>0x00000010</dt> </dl>                            | Disegna la maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**ILD \_ Immagine**</dt> <dt>0x00000020</dt> </dl>                         | Se la sovrapposizione non richiede il disegno di una maschera, impostare questo flag.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**ILD \_ ROP**</dt> <dt>0x00000040</dt> </dl>                               | Disegna l'immagine usando il codice dell'operazione raster specificato dal **membro dwRop.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**ILD \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Per estrarre l'immagine di sovrimpressione dal membro **fStyle,** usare l'and logico per combinare **fStyle** con il **valore ILD \_ OVERLAYMASK.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**ILD \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Mantiene il canale alfa nella destinazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**ILD \_ Scalabilità**</dt> <dt>0x00002000</dt> </dl>                         | Fa sì che l'immagine venga ridimensionata in cx, cy anziché ritagliata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**ILD \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Ridimensiona l'immagine in base al valore dpi corrente della visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**ILD \_ ASYNC**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista e versioni successive.** Disegnare l'immagine se disponibile nella cache. Non estrarlo automaticamente. Il metodo draw chiamato restituisce E PENDING al componente chiamante, che deve quindi eseguire un'azione alternativa, ad esempio fornire un'altra immagine e accodare un'attività in background per forzare il caricamento dell'immagine tramite \_ [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) usando il flag ALWAYS ILFIP. \_ Il flag ASYNC ILD impedisce quindi all'operazione di estrazione di bloccare il thread corrente ed è particolarmente importante se viene chiamato un metodo di disegno dal thread dell'interfaccia \_ utente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

