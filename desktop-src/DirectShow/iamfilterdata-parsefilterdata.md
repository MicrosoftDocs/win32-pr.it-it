---
description: Informazioni sul metodo IAMFilterData::P arseFilterData, decomprime i dati binari del Registro di sistema per un filtro. Questa interfaccia è stata deprecata.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Metodo IAMFilterData::P arseFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989446"
---
# <a name="iamfilterdataparsefilterdata-method"></a>Metodo IAMFilterData::P arseFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni non devono usarlo.

 

Il `ParseFilterData` metodo decomprime i dati binari del Registro di sistema per un filtro.

In genere non esiste alcun motivo per cui un'applicazione chiami questo metodo. Il [**metodo IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) offre un modo più pratico per accedere ai dati del Registro di sistema di filtro.

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

*rgbFilterData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati binari del Registro di sistema. È possibile ottenere questi dati recuperando la proprietà "FilterData" dal moniker di filtro. I dati vengono archiviati come **SAFEARRAY** di byte (VT \_ UI1 \| VT \_ ARRAY).

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Specifica le dimensioni dei dati binari, in byte.

</dd> <dt>

*prgbRegFilter2* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati decompressi. Quando il metodo viene restituito, eseguire il cast di questo puntatore a [**un tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) per accedere ai dati del filtro. Il chiamante deve rilasciare la memoria chiamando il **metodo CoTaskMemFree.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) nella Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




