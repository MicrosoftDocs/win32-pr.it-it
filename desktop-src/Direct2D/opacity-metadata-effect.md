---
title: Effetto dei metadati di opacità
description: È possibile usare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che siano possibili ottimizzazioni del rendering interne per il grafico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be14699214337dc3f8c6e9e525f128a382c14ee479af08b99ea1f9eadd00041d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665321"
---
# <a name="opacity-metadata-effect"></a>Effetto dei metadati di opacità

È possibile usare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che siano possibili ottimizzazioni del rendering interne per il grafico.

> [!Note]  
> Questo effetto non modifica l'immagine stessa in modo che sia opaca. Modifica i dati associati all'immagine in modo che il renderer presupponga che l'area specificata sia opaca.

 

Il CLSID per questo effetto è CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                 | Tipo e valore predefinito                                                             | Descrizione                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ PROP \_ INPUT \_ OPAQUE \_ RECT <br/> | D2D1 \_ VECTOR \_ 4F<br/> (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX) <br/> | Parte dell'immagine di origine opaca. Il valore predefinito è l'intera immagine di input.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

