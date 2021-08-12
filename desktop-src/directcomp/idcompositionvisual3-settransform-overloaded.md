---
title: Metodi IdCompositionVisual3 SetTransform (Dcomp.h)
description: Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 3D usata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto di trasformazione.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
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
ms.openlocfilehash: 08b243704c3eabae528d475c92b924f6aecfba92f923b7190c085e3e89bd1f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281238"
---
# <a name="idcompositionvisual3settransform-methods"></a>Metodi IDCompositionVisual3::SetTransform

Imposta la proprietà Transform di questo oggetto visivo. La proprietà Transform specifica una trasformazione 3D usata per modificare il sistema di coordinate di questo oggetto visivo. La proprietà può specificare una matrice di trasformazione 4 per 4 o un oggetto di trasformazione.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                  | Descrizione                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform(D2D \_ MATRIX \_ 4X4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Imposta la proprietà Transform sulla matrice di trasformazione specificata.<br/>      |
| [**SetTransform(IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Imposta la proprietà Transform sull'oggetto trasformazione specificato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2012 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
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

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
