---
title: Effetto dei metadati di opacità
description: È possibile utilizzare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che sia possibile ottimizzare il rendering interno del grafico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120950"
---
# <a name="opacity-metadata-effect"></a>Effetto dei metadati di opacità

È possibile utilizzare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che sia possibile ottimizzare il rendering interno del grafico.

> [!Note]  
> Questo effetto non modifica l'immagine in modo che sia opaca. Modifica i dati associati all'immagine in modo che il renderer presupponga che l'area specificata sia opaca.

 

Il CLSID per questo effetto è CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                 | Tipo e valore predefinito                                                             | Descrizione                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ - \_ input \_ opaco \_ Rect <br/> | D2D1 \_ vector \_ 4F<br/> (-FLT \_ MAX,-FLT \_ Max, flt \_ Max, flt \_ max) <br/> | Parte dell'immagine di origine opaca. Il valore predefinito è l'intera immagine di input.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

