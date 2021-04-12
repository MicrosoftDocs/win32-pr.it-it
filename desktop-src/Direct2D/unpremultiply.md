---
title: Effetto Unpremultiply
description: Utilizzare questo effetto per convertire un'immagine da alfa premoltiplicato a unpremultiplied alfa.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effetto unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400825"
---
# <a name="unpremultiply-effect"></a>Effetto Unpremultiply

Utilizzare questo effetto per convertire un'immagine da alfa premoltiplicato a unpremultiplied alfa. L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` con `P' = {R/A, G/A, B/A, A}` nell'output.

Questo effetto non ha proprietà.

Il CLSID per questo effetto è CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Bitmap di output

La dimensione bitmap di output corrisponde alla dimensione bitmap di input.

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

 

 
