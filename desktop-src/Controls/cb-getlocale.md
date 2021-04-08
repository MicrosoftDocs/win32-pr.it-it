---
title: Messaggio CB_GETLOCALE (winuser. h)
description: Ottiene le impostazioni locali correnti della casella combinata. Le impostazioni locali vengono utilizzate per determinare l'ordinamento corretto del testo visualizzato per le caselle combinate con lo \_ stile di ordinamento CBS e il testo aggiunto tramite il \_ messaggio CB ADDSTRING.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Controlli di Windows Message CB_GETLOCALE
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048355"
---
# <a name="cb_getlocale-message"></a>\_Messaggio GETlocals CB

Ottiene le impostazioni locali correnti della casella combinata. Le impostazioni locali vengono utilizzate per determinare l'ordinamento corretto del testo visualizzato per le caselle combinate con lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) e il testo aggiunto tramite il messaggio [**CB \_ ADDSTRING**](cb-addstring.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica le impostazioni locali correnti della casella combinata. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il codice paese/area geografica e il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della lingua.

## <a name="remarks"></a>Commenti

L'identificatore di lingua è costituito da un identificatore di lingua e da un identificatore di lingua primaria. La macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) Ottiene l'identificatore della lingua principale e la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) Ottiene l'identificatore di lingua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_impostazioni locali CB**](cb-setlocale.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

