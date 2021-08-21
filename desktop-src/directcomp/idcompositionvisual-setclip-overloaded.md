---
title: Metodi IDCompositionVisual SetClip (Dcomp.h)
description: Imposta la proprietà Clip di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Metodi SetClip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 1cc1d0f24c30e6ec11ecaa40b0317109eddaf432ee311a5b9545f34f7afa8582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043059"
---
# <a name="idcompositionvisualsetclip-methods"></a>Metodi IDCompositionVisual::SetClip

Imposta la proprietà Clip di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato. La proprietà Clip limita il rendering del sottoalbero visivo che ha come radice questo oggetto visivo a un'area rettangolare.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                | Descrizione                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip(const D2D \_ RECT \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Imposta la proprietà Clip sull'area rettangolare specificata.<br/> |
| [**SetClip(IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Imposta la proprietà Clip sull'oggetto clip specificato.<br/>        |



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

[Ritaglio](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
