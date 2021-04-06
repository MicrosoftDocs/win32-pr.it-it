---
title: Messaggio TB_GETBUTTON (COMmctrl. h)
description: Recupera le informazioni sul pulsante specificato in una barra degli strumenti.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Controlli di Windows Message TB_GETBUTTON
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743962"
---
# <a name="tb_getbutton-message"></a>\_Messaggio GETBUTTON TB

Recupera le informazioni sul pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che riceve le informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





