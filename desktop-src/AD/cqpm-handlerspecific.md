---
title: Messaggio CQPM_HANDLERSPECIFIC (cmnquery. h)
description: Valore di base utilizzato per i messaggi privati del gestore di query.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475586"
---
# <a name="cqpm_handlerspecific-message"></a>\_Messaggio CQPM HANDLERSPECIFIC

Il **messaggio \_ HANDLERSPECIFIC di CQPM** è il valore di base utilizzato per i messaggi privati del gestore di query. Il gestore di query deve aggiungere questo valore ai messaggi privati per assicurarsi che non si verifichino conflitti di messaggi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene dati aggiuntivi del messaggio. Il contenuto di questo parametro è definito dal gestore di query.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene dati aggiuntivi del messaggio. Il contenuto di questo parametro è definito dal gestore di query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il significato del valore restituito è definito dal gestore di query.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





