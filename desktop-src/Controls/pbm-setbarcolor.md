---
title: Messaggio PBM_SETBARCOLOR (COMmctrl. h)
description: Imposta il colore della barra indicatore di stato nel controllo indicatore di stato.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Controlli di Windows Message PBM_SETBARCOLOR
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518286"
---
# <a name="pbm_setbarcolor-message"></a>\_Messaggio SETBARCOLOR PBM

Imposta il colore della barra indicatore di stato nel controllo indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **COLORREF** che specifica il nuovo colore della barra dell'indicatore di stato. Se si specifica il \_ valore predefinito CLR, l'indicatore di stato utilizzerà il colore predefinito della barra dell'indicatore di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore della barra dell'indicatore di stato precedente oppure il \_ valore predefinito CLR se il colore della barra dell'indicatore di stato è il colore predefinito.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





