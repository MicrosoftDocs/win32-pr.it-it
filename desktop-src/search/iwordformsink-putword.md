---
description: Inserisce il modulo Word originale nell'oggetto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: Metodo IWordFormSink::P utWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306099"
---
# <a name="iwordformsinkputword-method"></a>IWordFormSink::P metodo utWord

Inserisce il modulo Word originale nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwcInBuf* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene la forma alternativa finale di una parola, che è sempre la parola originale.

</dd> <dt>

*CWC* \[ in\]
</dt> <dd>

Numero di caratteri in *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | L'operazione è stata completata correttamente. <br/> |



 

## <a name="remarks"></a>Commenti

**PutWord** viene chiamato dal metodo [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) dell'implementazione di [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Questo metodo gestisce il formato originale di una parola e viene chiamato per ultimo. Tutte le forme alternative precedenti per una parola vengono inserite nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chiamando [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).

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

 

 
