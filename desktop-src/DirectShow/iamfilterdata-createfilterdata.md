---
description: Informazioni sul metodo IAMFilterData::CreateFilterData, che crea dati binari del Registro di sistema per un filtro. Questa interfaccia è stata deprecata.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: Metodo IAMFilterData::CreateFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 81c2ba3a56ba9c09a2ce7b23bcad1a83880e61256402c291b5aebde9988218c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428671"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>Metodo IAMFilterData::CreateFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni non devono usarlo.

 

Il `CreateFilterData` metodo crea dati binari del Registro di sistema per un filtro. Questi dati possono essere scritti nel Registro di sistema come sottochiave REG BINARY denominata FilterData, sotto la chiave \_ CLSID del filtro.

In genere non esiste alcun motivo per cui un'applicazione chiami questo metodo. Il [**metodo IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automaticamente i dati binari e li aggiunge al percorso corretto nel Registro di sistema. Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

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

*prf2* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) che contiene le informazioni sul filtro.

</dd> <dt>

*prgbFilterData* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati binari. Il metodo alloca la memoria per i dati. Il chiamante deve rilasciare la memoria chiamando il **metodo CoTaskMemFree.**

</dd> <dt>

*pcb* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati binari, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) in Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




