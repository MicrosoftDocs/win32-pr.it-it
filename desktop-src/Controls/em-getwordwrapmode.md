---
title: Messaggio di EM_GETWORDWRAPMODE (RichEdit. h)
description: Ottiene il ritorno a capo automatico e le opzioni di Word break per il controllo Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Controlli di Windows Message EM_GETWORDWRAPMODE
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475568"
---
# <a name="em_getwordwrapmode-message"></a>\_Messaggio GETWORDWRAPMODE em

Ottiene il ritorno a capo automatico e le opzioni di Word break per il controllo Rich Edit.

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

Il messaggio restituisce le opzioni di ritorno a capo e di Word Breaking correnti.

## <a name="remarks"></a>Commenti

Questo messaggio non deve essere inviato dalla procedura di Word break definita dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





