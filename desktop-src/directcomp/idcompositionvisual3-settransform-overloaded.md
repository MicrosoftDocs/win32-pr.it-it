---
title: Metodi di trasformazione IDCompositionVisual3 (Dcomp. h)
description: Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 3D utilizzata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto Transform.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Metodi di trasformazione DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301722"
---
# <a name="idcompositionvisual3settransform-methods"></a>Metodi IDCompositionVisual3:: setransform

Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 3D utilizzata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto Transform.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                  | Descrizione                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Setransform (D2D \_ Matrix \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Imposta la proprietà Transform sulla matrice di trasformazione specificata.<br/>      |
| [**Setransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Imposta la proprietà Transform sull'oggetto Transformation specificato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Dcomp. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Dcomp. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

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

[**IDCompositionVisual:: seoffsety**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
