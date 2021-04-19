---
description: 'Il metodo Block blocca o Sblocca il flusso di dati dal pin. Questo metodo implementa il metodo IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Metodo CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333458"
---
# <a name="cdynamicoutputpinblock-method"></a>Metodo CDynamicOutputPin. Block

Il `Block` metodo blocca o Sblocca il flusso di dati dal pin. Questo metodo implementa il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

Flag che indica se bloccare o sbloccare il PIN. Deve essere uno dei valori seguenti: 

Zero: Sblocca il flusso di dati dal pin.

\_ \_ \_ \_ Blocco di controllo del flusso del pin am: blocca il flusso di dati dal pin.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle per un oggetto evento o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                                        | PIN già sbloccato.<br/>                     |
| <dl> <dt>**\_OK**</dt> </dl>                                           | Esito positivo.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argomento non valido.<br/>                             |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt> </dl>                   | Il PIN è già bloccato in un altro thread.<br/>     |
| <dl> <dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt> </dl> | Il PIN è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su questo metodo, vedere [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Internamente, questo metodo chiama uno dei metodi protetti seguenti:

-   Block (asincrono): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Blocco (sincrono): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Sblocco: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

Lo sblocco viene sempre eseguito in modo sincrono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




