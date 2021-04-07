---
title: IMAGELISTDRAWFLAGS (COMmctrl. h)
description: Passato al metodo di IImageList di richiamo nel membro fStyle di IMAGELISTDRAWPARAMS.
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
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964045"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Passato al metodo [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) nel membro **fStyle** di [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Costante/valore                                                                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000000</dt> normale </dl>                      | Disegna l'immagine utilizzando il colore di sfondo per l'elenco di immagini. Se il colore di sfondo è il \_ valore CLR None, l'immagine viene disegnata in modo trasparente utilizzando la maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000001</dt> trasparente </dl>       | Disegna l'immagine in modo trasparente utilizzando la maschera, indipendentemente dal colore di sfondo. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000002</dt> BLEND25 </dl>                   | Disegna l'immagine, fondendo il 25% con il colore di Blend specificato da **rgbFg**. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000002</dt> lo stato attivo </dl>                         | Uguale a **ILD \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000004</dt> BLEND50 </dl>                   | Disegna l'immagine, fondendo il 50% con il colore di Blend specificato da **rgbFg**. Questo valore non ha alcun effetto se l'elenco di immagini non contiene una maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000004</dt> selezionato </dl>                | Uguale a **ILD \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000004</dt> di Blend </dl>                         | Uguale a **ILD \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**ILD \_ MASCHERA**</dt> <dt>0x00000010</dt> </dl>                            | Disegna la maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000020</dt> immagine </dl>                         | Se per la sovrimpressione non è necessaria la traccia di una maschera, impostare questo flag.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000040</dt> por </dl>                               | Disegna l'immagine usando il codice dell'operazione raster specificato dal membro **dwRop** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**ILD \_**</dt> <dt>0x00000F00</dt> OVERLAYMASK </dl>       | Per estrarre l'immagine sovrapposta dal membro **fStyle** , usare l'operatore logico and per combinare **fStyle** con il valore **ILD \_ OVERLAYMASK** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**ILD \_**</dt> <dt>0x00001000</dt> PRESERVEALPHA </dl> | Conserva il canale alfa nella destinazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**ILD \_ RIDIMENSIONAre**</dt> <dt>0x00002000</dt> </dl>                         | Fa in modo che l'immagine venga ridimensionata a CX, CY anziché ritagliata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**ILD \_**</dt> <dt>0x00004000</dt> DPISCALE </dl>                | Ridimensiona l'immagine al valore dpi corrente della visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**ILD \_**</dt> <dt>0x00008000</dt> asincrono </dl>                         | **Windows Vista e versioni successive.** Creare l'immagine se è disponibile nella cache. Non estrarlo automaticamente. Il metodo di creazione chiamato restituisce E \_ in sospeso al componente chiamante, che dovrebbe quindi eseguire un'azione alternativa, ad esempio, fornire un'altra immagine e accodare un'attività in background per forzare il caricamento dell'immagine tramite [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) usando il \_ flag ILFIP always. Il \_ flag asincrono ILD impedisce quindi all'operazione di estrazione di bloccare il thread corrente ed è particolarmente importante se un metodo di traccia viene chiamato dal thread dell'interfaccia utente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

