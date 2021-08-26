---
title: Metodi di ridimensionamento ID2D1HwndRenderTarget (D2d1.h)
description: Modifica le dimensioni della destinazione di rendering alle dimensioni in pixel specificate.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Metodi di ridimensionamento Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 31ffcae6473924e12ca428fd48927fd1507840dce4fdbce3a18e8f82ffe9fcaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917611"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>Metodi ID2D1HwndRenderTarget::Resize

Modifica le dimensioni della destinazione di rendering alle dimensioni in pixel specificate.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                         | Descrizione                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Resize(D2D1 \_ SIZE \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Modifica le dimensioni della destinazione di rendering alle dimensioni in pixel specificate. <br/> |
| [**Resize(D2D1 \_ SIZE \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Modifica le dimensioni della destinazione di rendering alle dimensioni in pixel specificate.<br/>  |



## <a name="remarks"></a>Commenti

Dopo la chiamata a questo metodo, il contenuto del buffer nascosto della destinazione di rendering non viene definito, anche se è stata specificata l'opzione [**D2D1 \_ PRESENT OPTIONS RETAIN \_ \_ \_ CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) al momento della creazione della destinazione di rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
