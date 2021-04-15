---
title: Messaggio LB_GETLOCALE (winuser. h)
description: Ottiene le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo \_ stile di ordinamento lbs) e del testo aggiunto dal \_ messaggio ADDSTRING lb.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Controlli di Windows Message LB_GETLOCALE
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477290"
---
# <a name="lb_getlocale-message"></a>LB \_ GetLocale messaggio

Ottiene le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) ) e del testo aggiunto dal [**messaggio \_ ADDSTRING lb**](lb-addstring.md) .

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

Il valore restituito specifica le impostazioni locali correnti della casella di riepilogo. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il codice paese/area geografica e il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della lingua.

## <a name="remarks"></a>Commenti

L'identificatore della lingua è costituito da un identificatore di lingua e da un identificatore di lingua primaria. Utilizzare la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) per estrarre l'identificatore di lingua principale da [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) per estrarre l'identificatore del linguaggio di sottolinguaggio.

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

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**\_impostazioni locali lb**](lb-setlocale.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

