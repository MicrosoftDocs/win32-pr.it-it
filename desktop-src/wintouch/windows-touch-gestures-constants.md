---
title: Costanti movimenti tocco di Windows (winuser. h)
description: In questa sezione sono elencate le costanti utilizzate per i movimenti tocco di Windows.
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964265"
---
# <a name="windows-touch-gestures-constants"></a>Costanti movimenti tocco di Windows

In questa sezione sono elencate le costanti utilizzate per i movimenti tocco di Windows.

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

Definisce il numero massimo di configurazioni di movimento che possono essere incluse in una singola chiamata a [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) o [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [movimenti tocco di Windows](multi-touch-gestures.md)
