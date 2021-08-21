---
title: Metodo GetLicenseState IWMDRMDevice2
description: Il metodo GetLicenseState ottiene lo stato della licenza.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Metodo GetLicenseState windows Media Device Manager
- Metodo GetLicenseState windows Media Device Manager , interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 windows Media Device Manager, metodo GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e068d537f460053800b0d52d667ba39b0577d717b08f83794a73b2bf8c854aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055699"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>Metodo IWMDRMDevice2::GetLicenseState

Il **metodo GetLicenseState** ottiene lo stato della licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbStateQueryData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati sottoposti a query dello stato della licenza.

</dd> <dt>

*cbStateQueryData* \[ Pollici\]
</dt> <dd>

Conteggio dei dati sottoposti a query.

</dd> <dt>

*pdwCategory* \[ Cambio\]
</dt> <dd>

Puntatore alla categoria.

</dd> <dt>

*pcRemainingCounts* \[ Cambio\]
</dt> <dd>

Puntatore ai conteggi rimanenti.

</dd> <dt>

*pcRemainingHours* \[ Cambio\]
</dt> <dd>

Puntatore alle ore rimanenti.

</dd> <dt>

*pdwReserved* \[ Cambio\]
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo ha esito positivo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





