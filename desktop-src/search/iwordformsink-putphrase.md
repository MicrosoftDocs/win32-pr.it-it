---
description: Inserisce una forma alternativa di una parola nell'oggetto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: Metodo IWordFormSink::P utAltWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750359"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink::P metodo utAltWord

Inserisce una forma alternativa di una parola nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwcInBuf* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene una forma alternativa di una parola.

</dd> <dt>

*CWC* \[ in\]
</dt> <dd>

Numero di caratteri in *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                              | Descrizione                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | L'operazione è stata completata correttamente. <br/>                                                                                             |
| <dl> <dt>**Lingua \_ di \_ \_ parola grande**</dt> </dl> | Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) dell'implementazione di [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Tutte le forme alternative per una parola, eccetto le ultime, vengono inserite nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chiamando **IWordFormSink::P utaltword**. Il formato alternativo finale di una parola, che è sempre il formato originale della parola, viene gestito chiamando [**IWordFormSink::P utword**](iwordformsink-putword.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
