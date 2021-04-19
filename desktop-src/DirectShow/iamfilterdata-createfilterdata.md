---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Metodo IAMFilterData:: CreateFilterData (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326819"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>Metodo IAMFilterData:: CreateFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni non devono utilizzarlo.

 

Il `CreateFilterData` metodo crea dati del registro di sistema binari per un filtro. Questi dati possono essere scritti nel registro di sistema come una \_ sottochiave reg Binary denominata FilterData, sotto la chiave CLSID del filtro.

Non esiste in genere un motivo per cui un'applicazione chiama questo metodo. Il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automaticamente i dati binari e li aggiunge alla posizione corretta nel registro di sistema. Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PRF2* \[ in\]
</dt> <dd>

Puntatore a una struttura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) che contiene le informazioni sul filtro.

</dd> <dt>

*prgbFilterData* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati binari. Il metodo alloca la memoria per i dati. Il chiamante deve rilasciare la memoria chiamando il metodo **CoTaskMemFree** .

</dd> <dt>

*PCB* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati binari, in byte.

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

 

 




