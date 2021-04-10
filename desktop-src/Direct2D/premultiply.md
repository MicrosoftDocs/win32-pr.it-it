---
title: Effetto premoltiplicato
description: Utilizzare questo effetto per convertire un'immagine da unpremultiplied alfa a alfa premoltiplicato.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- effetto premoltiplicato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964536"
---
# <a name="premultiply-effect"></a>Effetto premoltiplicato

Utilizzare questo effetto per convertire un'immagine da unpremultiplied alfa a alfa premoltiplicato. L'effetto sostituisce ogni pixel di input `P = {R, G, B, A}` con `P' = {R*A, G*A, B*A, A}` nell'output.

Questo effetto non ha proprietà.

Il CLSID per questo effetto è CLSID \_ D2D1Premultiply.

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

 

 
