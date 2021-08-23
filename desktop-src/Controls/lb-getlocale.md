---
title: LB_GETLOCALE messaggio (Winuser.h)
description: Ottiene le impostazioni locali correnti della casella di riepilogo. È possibile usare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile LBS SORT) e del testo aggiunto dal messaggio \_ \_ LB ADDSTRING.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE di controllo Windows messaggio
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
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544521"
---
# <a name="lb_getlocale-message"></a>Messaggio \_ LB GETLOCALE

Ottiene le impostazioni locali correnti della casella di riepilogo. È possibile usare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile [**\_ LBS SORT)**](list-box-styles.md) e del testo aggiunto dal messaggio [**\_ LB ADDSTRING.**](lb-addstring.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica le impostazioni locali correnti della casella di riepilogo. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il codice paese/area geografica e [**il valore LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della lingua.

## <a name="remarks"></a>Commenti

L'identificatore di lingua è costituito da un identificatore di sottolingua e da un identificatore di lingua principale. Usare la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) per estrarre l'identificatore di lingua principale dalla [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) per estrarre l'identificatore della sottolingua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

