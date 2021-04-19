---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData: metodo:P arseFilterData (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326817"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData::P metodo arseFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni non devono utilizzarlo.

 

Il `ParseFilterData` Metodo decomprime i dati del registro di sistema binario per un filtro.

Non esiste in genere un motivo per cui un'applicazione chiama questo metodo. Il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornisce un modo più pratico per accedere ai dati del registro di sistema del filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rgbFilterData* \[ in\]
</dt> <dd>

Puntatore ai dati binari del registro di sistema. È possibile ottenere questi dati recuperando la proprietà "FilterData" dal moniker del filtro. I dati vengono archiviati come **SAFEARRAY** di byte (VT \_ Ui1 \| VT \_ Array).

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Specifica le dimensioni in byte dei dati binari.

</dd> <dt>

*prgbRegFilter2* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati decompressi. Quando il metodo restituisce un risultato, eseguire il cast di questo puntatore a un tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) per accedere ai dati del filtro. Il chiamante deve rilasciare la memoria chiamando il metodo **CoTaskMemFree** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> L'intestazione fil \_ Data. h si trova nella directory degli [esempi del Mapper](mapper-sample.md) nel Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




