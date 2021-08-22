---
description: Il metodo Block blocca o sblocca il flusso di dati dal pin. Questo metodo implementa il metodo IPinFlowControl::Block.
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Metodo CDynamicOutputPin.Block (Amfilter.h)
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
ms.openlocfilehash: 6cc0a601ee1adbff9254baeff029c26d0cea359c7b2770b4d518bad916aca09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074285"
---
# <a name="cdynamicoutputpinblock-method"></a>Metodo CDynamicOutputPin.Block

Il `Block` metodo blocca o sblocca il flusso di dati dal pin. Questo metodo implementa il [**metodo IPinFlowControl::Block.**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block)

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

Flag che indica se bloccare o sbloccare il pin. Deve essere uno dei valori seguenti: 

Zero: sblocca il flusso di dati dal pin.

AM \_ PIN FLOW CONTROL \_ \_ \_ BLOCK: blocca il flusso di dati dal pin.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle per un oggetto evento o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                                    | Descrizione                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                                        | Il pin è già sbloccato.<br/>                     |
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Operazione completata.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argomento non valido.<br/>                             |
| <dl> <dt>**PIN \_ VFW E \_ GIÀ \_ \_ BLOCCATO**</dt> </dl>                   | L'aggiunta è già bloccata in un altro thread.<br/>     |
| <dl> <dt>**IL \_ PIN VFW E È GIÀ BLOCCATO IN QUESTO \_ \_ \_ \_ \_ \_ THREAD**</dt> </dl> | Il pin è già bloccato nel thread chiamante.<br/> |



 

## <a name="remarks"></a>Commenti

Per altre informazioni su questo metodo, vedere [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Internamente, questo metodo chiama uno dei metodi protetti seguenti:

-   Block (asincrono): [ **CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Block (sincrono): [ **CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Sblocco: [ **CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

Lo sblocco viene sempre eseguito in modo sincrono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




