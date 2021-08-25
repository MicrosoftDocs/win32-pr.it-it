---
title: Metodo IConfigAsfWriter2 StreamNumFromPin
description: Il metodo StreamNumFromPin recupera il numero di flusso associato al pin di input specificato.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Metodo StreamNumFromPin windows Media Format
- Metodo StreamNumFromPin windows Media Format , interfaccia IConfigAsfWriter2
- Metodo StreamNumFromPin dell'interfaccia IConfigAsfWriter2 di Windows Media Format
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839822"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Metodo IConfigAsfWriter2::StreamNumFromPin

Il **metodo StreamNumFromPin** recupera il numero di flusso associato al pin di input specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* \[ Pollici\]
</dt> <dd>

Puntatore **all'interfaccia IPin** sul pin di input.

</dd> <dt>

*pwStreamNum* \[ Cambio\]
</dt> <dd>

Puntatore che riceve il numero di flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se non riesce, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

In alcuni casi potrebbe essere necessario usare direttamente le interfacce Windows Media Format SDK per modificare un flusso prima di eseguire un grafico di filtro. Poiché non è possibile presupporre che un numero di flusso ASF sia lo stesso DirectShow pin, viene fornito questo metodo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 