---
description: Il metodo ReceiveCanBlock determina se le chiamate al metodo IMemInputPin::Receive possono bloccarsi. Questo metodo implementa il metodo IMemInputPin::ReceiveCanBlock.
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Metodo CBaseInputPin.ReceiveCanBlock (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ece7243c145d34ed06e29b2a29ae9847e682981337b96a47976c20eb76272d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823853"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>Metodo CBaseInputPin.ReceiveCanBlock

Il `ReceiveCanBlock` metodo determina se le chiamate al metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) possono bloccarsi. Questo metodo implementa il [**metodo IMemInputPin::ReceiveCanBlock.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori includono quelli elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il pin non si blocerà in una chiamata a **Receive**.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Il pin potrebbe bloccarsi in una chiamata a **Receive**.<br/>    |



 

## <a name="remarks"></a>Commenti

Restituisce S \_ FALSE se è garantito che le chiamate **al metodo Receive** non si blocchino. In caso contrario, restituire S \_ OK o un codice di errore. Se il **metodo Receive** chiama **Receive** su un pin downstream, il pin downstream potrebbe bloccarsi; `ReceiveCanBlock` deve prendere in considerazione tale fattore.

Un filtro upstream può usare questo metodo per determinare la strategia di threading. Se il **metodo Receive** potrebbe bloccarsi, il filtro upstream potrebbe decidere di usare un thread di lavoro che esegue il buffer dei dati. Per [**un'implementazione di questa**](coutputqueue.md) strategia, vedere la classe COutputQueue .

Nella classe di base questo metodo restituisce S OK quando si verifica una delle \_ condizioni seguenti:

-   Il filtro non ha pin di output.
-   Un pin di input connesso a questo filtro segnala che potrebbe bloccarsi.
-   Un pin di input connesso a questo filtro non supporta [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




