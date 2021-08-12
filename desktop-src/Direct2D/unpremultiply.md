---
title: Effetto non premoltimultipamente
description: Usare questo effetto per convertire un'immagine da alfa premoltilied a alfa non premoltitipli.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effetto nonpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664879"
---
# <a name="unpremultiply-effect"></a>Effetto non premoltimultipamente

Usare questo effetto per convertire un'immagine da alfa premoltilied a alfa non premoltitipli. L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` `P' = {R/A, G/A, B/A, A}` con nell'output.

Questo effetto non ha proprietà.

Il CLSID per questo effetto è CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output sono le stesse della bitmap di input.

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

 

 
