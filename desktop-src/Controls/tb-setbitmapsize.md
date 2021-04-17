---
title: Messaggio TB_SETBITMAPSIZE (COMmctrl. h)
description: Imposta la dimensione delle immagini bitmap da aggiungere a una barra degli strumenti.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Controlli di Windows Message TB_SETBITMAPSIZE
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475137"
---
# <a name="tb_setbitmapsize-message"></a>TB \_ SETBITMAPSIZE messaggio

Imposta la dimensione delle immagini bitmap da aggiungere a una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza, in pixel, delle immagini bitmap. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'altezza, in pixel, delle immagini bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

È possibile impostare le dimensioni solo prima di aggiungere bitmap alla barra degli strumenti. Se le dimensioni della bitmap non vengono impostate in modo esplicito in un'applicazione, le dimensioni predefinite sono pari a 16 per 15 pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

