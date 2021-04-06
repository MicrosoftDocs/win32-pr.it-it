---
title: Metodi di IDCompositionVisual (Dcomp. h)
description: Imposta la proprietà di ritaglio di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Metodi di seclip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743410"
---
# <a name="idcompositionvisualsetclip-methods"></a>Metodi IDCompositionVisual:: seclip

Imposta la proprietà di ritaglio di questo oggetto visivo sull'area rettangolare o sull'oggetto clip specificato. La proprietà clip limita il rendering della sottostruttura ad albero visuale che è radicata in questo oggetto visivo in un'area rettangolare.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                | Descrizione                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Seclip (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Imposta la proprietà clip sull'area rettangolare specificata.<br/> |
| [**Seclip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Imposta la proprietà di ritaglio sull'oggetto clip specificato.<br/>        |



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

[Ritaglio](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
