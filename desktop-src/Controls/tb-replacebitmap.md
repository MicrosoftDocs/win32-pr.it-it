---
title: Messaggio TB_REPLACEBITMAP (COMmctrl. h)
description: Sostituisce una bitmap esistente con una nuova bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- Controlli di Windows Message TB_REPLACEBITMAP
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874210"
---
# <a name="tb_replacebitmap-message"></a>TB \_ REPLACEBITMAP messaggio

Sostituisce una bitmap esistente con una nuova bitmap.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) che contiene le informazioni della bitmap da sostituire e la nuova bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





