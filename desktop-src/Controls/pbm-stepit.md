---
title: Messaggio PBM_STEPIT (COMmctrl. h)
description: Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegnato la barra per riflettere la nuova posizione. Un'applicazione consente di impostare l'incremento del passaggio inviando il \_ messaggio di SEPASSO PBM.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Controlli di Windows Message PBM_STEPIT
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964560"
---
# <a name="pbm_stepit-message"></a>\_Messaggio STEPIT PBM

Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegnato la barra per riflettere la nuova posizione. Un'applicazione consente di impostare l'incremento del passaggio inviando il messaggio di [**\_ sepasso PBM**](pbm-setstep.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione precedente.

## <a name="remarks"></a>Commenti

Quando la posizione supera il valore di intervallo massimo, questo messaggio Reimposta la posizione corrente in modo che l'indicatore di stato ricominci dall'inizio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





