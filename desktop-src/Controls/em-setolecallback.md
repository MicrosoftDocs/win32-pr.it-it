---
title: Messaggio di EM_SETOLECALLBACK (RichEdit. h)
description: Fornisce un controllo Rich Edit di un oggetto IRichEditOleCallback che il controllo utilizza per ottenere le informazioni e le risorse correlate a OLE dal client.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Controlli di Windows Message EM_SETOLECALLBACK
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964389"
---
# <a name="em_setolecallback-message"></a>\_Messaggio SETOLECALLBACK em

Fornisce un controllo Rich Edit di un oggetto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) che il controllo utilizza per ottenere le informazioni e le risorse correlate a OLE dal client.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un oggetto [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) . Il controllo chiama il metodo [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) per l'oggetto prima della restituzione.

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



 

