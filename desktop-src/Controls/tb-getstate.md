---
title: Messaggio TB_GETSTATE (COMmctrl. h)
description: Recupera le informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Controlli di Windows Message TB_GETSTATE
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873474"
---
# <a name="tb_getstate-message"></a>TB- \_ messaggio di stato

Recupera le informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le informazioni sullo stato del pulsante in caso di esito positivo o-1 in caso contrario. Le informazioni sullo stato del pulsante possono essere una combinazione dei valori elencati negli [**stati dei pulsanti della barra degli strumenti**](toolbar-button-states.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





