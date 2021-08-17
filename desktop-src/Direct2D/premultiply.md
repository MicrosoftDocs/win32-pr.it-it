---
title: Effetto premoltimultiply
description: Usare questo effetto per convertire un'immagine da alfa non premoltimullied a alfa premoltimullied.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- effetto premultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af158ab8f885c51d2dce15d5bfbc5c24f34f6a980ebc8e8f4631617d31a2a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075025"
---
# <a name="premultiply-effect"></a>Effetto premoltimultiply

Usare questo effetto per convertire un'immagine da alfa non premoltimullied a alfa premoltimullied. L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` `P' = {R*A, G*A, B*A, A}` con nell'output.

Questo effetto non ha proprietà.

Il CLSID per questo effetto è CLSID \_ D2D1Premultiply.

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output sono le stesse delle dimensioni della bitmap di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
