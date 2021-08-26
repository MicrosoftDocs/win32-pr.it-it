---
title: LVM_GETGROUPMETRICS messaggio (Commctrl.h)
description: Ottiene informazioni sulla visualizzazione dei gruppi.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS di Windows di messaggi
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b99996adfe7f26342dde8967c95973fdb972290367328875257f5615f0a43c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062611"
---
# <a name="lvm_getgroupmetrics-message"></a>Messaggio LVM \_ GETGROUPMETRICS

Ottiene informazioni sulla visualizzazione dei gruppi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**struttura LVGROUPMETRICS**</a> che riceve le metriche recuperate.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





