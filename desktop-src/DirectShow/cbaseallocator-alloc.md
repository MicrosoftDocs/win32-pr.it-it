---
description: 'Metodo CBaseAllocator.Alloc: il metodo Alloc alloca memoria per i buffer.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Metodo CBaseAllocator.Alloc (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096368"
---
# <a name="cbaseallocatoralloc-method"></a>Metodo CBaseAllocator.Alloc

Il `Alloc` metodo alloca memoria per i buffer.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                       | Descrizione                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>           | I requisiti del buffer non sono stati modificati.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>              | I requisiti del buffer sono stati modificati.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | I requisiti del buffer non sono stati impostati.<br/>     |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal [**metodo CBaseAllocator::Commit.**](cbaseallocator-commit.md)

Nella classe di base questo metodo non alloca memoria. Restituisce un errore se i requisiti del buffer non sono stati impostati, S FALSE se i requisiti non sono stati modificati e S OK se \_ i requisiti sono stati \_ modificati.

Una classe derivata deve eseguire l'override di questo metodo per eseguire l'allocazione di memoria effettiva. In genere, la classe derivata esegue i passaggi seguenti:

1.  Chiamare l'implementazione della classe di base per determinare se la memoria richiede effettivamente l'allocazione.
2.  Allocare memoria.
3.  Creare [**oggetti CMediaSample**](cmediasample.md) che contengono blocchi di memoria dal passaggio 2.
4.  Aggiungere ogni **oggetto CMediaSample** all'elenco di esempi gratuiti ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).

Per un esempio, vedere [**CMemAllocator::Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




