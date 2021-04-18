---
title: Metodi di ridimensionamento ID2D1HwndRenderTarget (D2d1. h)
description: Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Ridimensiona metodi Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330071"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>Metodi ID2D1HwndRenderTarget:: Resize

Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                         | Descrizione                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Ridimensiona (D2D1 \_ dimensioni \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata. <br/> |
| [**Ridimensiona (D2D1 \_ dimensioni \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.<br/>  |



## <a name="remarks"></a>Commenti

Dopo la chiamata a questo metodo, il contenuto del back-buffer della destinazione di rendering non è definito, anche se è stata specificata l'opzione [**\_ \_ \_ Mantieni \_ contenuto d2d1 opzioni presenti**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) durante la creazione della destinazione di rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
