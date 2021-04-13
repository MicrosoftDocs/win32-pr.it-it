---
title: Metodo IConfigAsfWriter2 StreamNumFromPin
description: Il metodo StreamNumFromPin Recupera il numero di flusso associato al pin di input specificato.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Metodo StreamNumFromPin Windows Media Format
- Metodo StreamNumFromPin Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399161"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Metodo IConfigAsfWriter2:: StreamNumFromPin

Il metodo **StreamNumFromPin** Recupera il numero di flusso associato al pin di input specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* \[ in\]
</dt> <dd>

Puntatore all'interfaccia **Ipin** sul pin di input.

</dd> <dt>

*pwStreamNum* \[ out\]
</dt> <dd>

Puntatore che riceve il numero di flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

In alcuni casi potrebbe essere necessario usare direttamente le interfacce SDK di formato Windows Media per modificare un flusso prima di eseguire un grafico di filtro. Poiché non è possibile presupporre che un numero di flusso ASF corrisponda al numero del pin DirectShow, viene fornito questo metodo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 