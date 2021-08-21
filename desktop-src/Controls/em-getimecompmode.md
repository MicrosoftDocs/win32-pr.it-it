---
title: EM_GETIMECOMPMODE messaggio (Richedit.h)
description: Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE di controllo Windows messaggio
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
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019549"
---
# <a name="em_getimecompmode-message"></a>Messaggio \_ EM GETIMECOMPMODE

Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei valori seguenti.



| Codice restituito                                                                                     | Descrizione                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_ICM NOTOPEN**</dt> </dl>     | L'IME non è aperto.<br/>  |
| <dl> <dt>**\_ICM LEVEL3**</dt> </dl>      | True in modalità inline.<br/> |
| <dl> <dt>**\_ICM LEVEL2**</dt> </dl>      | Livello 2.<br/>          |
| <dl> <dt>**\_ICM LIVELLO \_ 2 5**</dt> </dl>   | Livello 2.5<br/>         |
| <dl> <dt>**\_ICM LEVEL2 \_ SUI**</dt> </dl> | Interfaccia utente speciale.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





