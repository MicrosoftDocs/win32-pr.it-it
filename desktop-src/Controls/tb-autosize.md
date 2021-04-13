---
title: Messaggio TB_AUTOSIZE (COMmctrl. h)
description: Determina il ridimensionamento di una barra degli strumenti.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Controlli di Windows Message TB_AUTOSIZE
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519310"
---
# <a name="tb_autosize-message"></a>\_Messaggio AUTOSIZE TB

Determina il ridimensionamento di una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione invia il messaggio di **\_ ridimensionamento automatico TB** dopo aver causato la modifica delle dimensioni di una barra degli strumenti impostando le dimensioni del pulsante o della bitmap oppure aggiungendo stringhe per la prima volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





