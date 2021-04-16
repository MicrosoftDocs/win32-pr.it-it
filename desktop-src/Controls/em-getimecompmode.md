---
title: Messaggio di EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Controlli di Windows Message EM_GETIMECOMPMODE
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477914"
---
# <a name="em_getimecompmode-message"></a>\_Messaggio GETIMECOMPMODE em

Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei valori seguenti.



| Codice restituito                                                                                     | Descrizione                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_NOTOPEN ICM**</dt> </dl>     | IME non è aperto.<br/>  |
| <dl> <dt>**\_Level3 ICM**</dt> </dl>      | Modalità in linea true.<br/> |
| <dl> <dt>**\_Level2 ICM**</dt> </dl>      | Livello 2.<br/>          |
| <dl> <dt>**ICM \_ Level2 \_ 5**</dt> </dl>   | Livello 2,5<br/>         |
| <dl> <dt>**ICM \_ Level2 \_ sui**</dt> </dl> | Interfaccia utente speciale.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





