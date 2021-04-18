---
description: Inserisce una parola e la relativa posizione nell'oggetto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Metodo IWordSink::P utWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306095"
---
# <a name="iwordsinkputword-method"></a>IWordSink::P metodo utWord

Inserisce una parola e la relativa posizione nell'oggetto [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CWC* \[ in\]
</dt> <dd>

Numero di caratteri in *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene una forma alternativa di una parola dal testo di origine. Questo parametro non viene modificato da **PutWord**. È possibile passare il parametro *pTextSource* da [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , in base alle esigenze.

</dd> <dt>

*cwcSrcLen* \[ in\]
</dt> <dd>

Il numero di caratteri nel buffer di testo di origine (indicato dal parametro *pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) che corrispondono alla parola contenuta in *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ in\]
</dt> <dd>

Posizione iniziale della parola in *pwcInBuf* nel buffer del testo di origine (indicata dal parametro *pTextSource* per [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                              | Descrizione                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | L'operazione è stata completata correttamente. Indica inoltre che non è disponibile altro testo per riempire il buffer.<br/>                                  |
| <dl> <dt>**Lingua \_ di \_ \_ parola grande**</dt> </dl> | Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Commenti

È consigliabile che il metodo **IWordSink::P utword** contenga sempre la parola originale come disponibile in *pTextSource*. Le forme alternative della parola vengono passate a WordSink usando [**IWordSink::P utaltword**](iwordsink-putaltword.md). Si consiglia inoltre di fare in modo che le parole in *pwcInBuf* corrispondano quanto più possibile al testo di origine. Ad esempio, se possibile, mantenere le lettere maiuscole e gli accenti.

Questa chiamata deve essere eseguita per ogni parola recuperata da *pTextSource* , ad eccezione di quelle per cui è stata effettuata la chiamata a [**IWordSink::P utaltword**](iwordsink-putaltword.md) . La parola viene terminata con un carattere EOW quando viene salvata in WordSink.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
