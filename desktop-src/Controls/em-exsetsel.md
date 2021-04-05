---
title: Messaggio di EM_EXSETSEL (RichEdit. h)
description: Seleziona un intervallo di caratteri o oggetti Component Object Model (COM) in un controllo Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Controlli di Windows Message EM_EXSETSEL
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874049"
---
# <a name="em_exsetsel-message"></a>\_Messaggio EXSETSEL em

Seleziona un intervallo di caratteri o oggetti Component Object Model (COM) in un controllo Microsoft Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che specifica l'intervallo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la selezione effettivamente impostata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





