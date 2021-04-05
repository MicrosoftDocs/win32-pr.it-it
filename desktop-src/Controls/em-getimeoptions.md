---
title: Messaggio di EM_GETIMEOPTIONS (RichEdit. h)
description: Recupera le opzioni IME (Input Method Editor) correnti.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Controlli di Windows Message EM_GETIMEOPTIONS
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120531"
---
# <a name="em_getimeoptions-message"></a>\_Messaggio GETIMEOPTIONS em

Recupera le opzioni IME (Input Method Editor) correnti.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive di Rich Edit.

 

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

Questo messaggio restituisce uno o più valori del flag di opzione IME descritti nel messaggio [**\_ SETIMEOPTIONS em**](em-setimeoptions.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETIMEOPTIONS em**](em-setimeoptions.md)
</dt> </dl>

 

 





