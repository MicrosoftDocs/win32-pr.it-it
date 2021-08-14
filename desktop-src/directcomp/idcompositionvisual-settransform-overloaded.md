---
title: Metodi IDCompositionVisual SetTransform (Dcomp.h)
description: Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 2D usata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 3 per 2 o un oggetto transform.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- Metodi SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b38c2e8fce2f0687b78b65574858a38bba681c6bc1174cab13dfa254e3b186c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281248"
---
# <a name="idcompositionvisualsettransform-methods"></a>Metodi IDCompositionVisual::SetTransform

Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 2D usata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 3 per 2 o un oggetto transform.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                    | Descrizione                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform(D2D \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Imposta la proprietà Transform sulla matrice di trasformazione specificata.<br/>      |
| [**SetTransform(IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Imposta la proprietà Transform sull'oggetto trasformazione specificato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2012 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
