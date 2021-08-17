---
title: EM_GETOLEINTERFACE messaggio (Richedit.h)
description: Recupera un oggetto IRichEditOle che un client può usare per accedere alla funzionalità Component Object Model (COM) di un controllo Rich Edit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e1799039081ed8250cb062aa3d1348a2fe8a8dbdcfa768fab74855d18d8e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831672"
---
# <a name="em_getoleinterface-message"></a>Messaggio \_ EM GETOLEINTERFACE

Recupera un [**oggetto IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) che un client può usare per accedere alla funzionalità Component Object Model (COM) di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un puntatore che riceve [**l'oggetto IRichEditOle.**](/windows/desktop/api/Richole/nn-richole-iricheditole) Il controllo chiama il [**metodo AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per l'oggetto prima della restituzione, quindi l'applicazione chiamante deve chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) al termine dell'operazione con l'oggetto .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

