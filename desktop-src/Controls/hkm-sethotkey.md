---
title: Messaggio HKM_SETHOTKEY (COMmctrl. h)
description: Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Controlli di Windows Message HKM_SETHOTKEY
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517650"
---
# <a name="hkm_sethotkey-message"></a>\_Messaggio SEHOTKEY HKM

Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta. [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) di **LOWORD** è il modificatore di chiave che indica le chiavi che definiscono una combinazione di tasti di scelta rapida. Per un elenco di valori dei flag di modifica, vedere la descrizione del messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

