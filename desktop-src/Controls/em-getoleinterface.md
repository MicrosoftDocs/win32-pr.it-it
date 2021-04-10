---
title: Messaggio di EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera un oggetto IRichEditOle che può essere utilizzato da un client per accedere a una funzionalità di Component Object Model (COM) del controllo Rich Edit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Controlli di Windows Message EM_GETOLEINTERFACE
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
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120530"
---
# <a name="em_getoleinterface-message"></a>\_Messaggio GETOLEINTERFACE em

Recupera un oggetto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) che può essere utilizzato da un client per accedere a una funzionalità di Component Object Model (com) del controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un puntatore che riceve l'oggetto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) . Il controllo chiama il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per l'oggetto prima della restituzione, quindi l'applicazione chiamante deve chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando viene eseguita con l'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

