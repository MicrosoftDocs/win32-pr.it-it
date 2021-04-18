---
title: Metodo IWMDRMDevice2 GetLicenseState
description: Il metodo GetLicenseState ottiene lo stato della licenza.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Metodo GetLicenseState Windows Media Gestione dispositivi
- Metodo GetLicenseState Windows Media Gestione dispositivi, interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 Windows Media Gestione dispositivi, metodo GetLicenseState
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
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333857"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>Metodo IWMDRMDevice2:: GetLicenseState

Il metodo **GetLicenseState** ottiene lo stato della licenza.

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

*pbStateQueryData* \[ in\]
</dt> <dd>

Puntatore ai dati sottoposti a query dello stato della licenza.

</dd> <dt>

*cbStateQueryData* \[ in\]
</dt> <dd>

Conteggio dei dati sottoposti a query.

</dd> <dt>

*pdwCategory* \[ out\]
</dt> <dd>

Puntatore alla categoria.

</dd> <dt>

*pcRemainingCounts* \[ out\]
</dt> <dd>

Puntatore ai conteggi rimanenti.

</dd> <dt>

*pcRemainingHours* \[ out\]
</dt> <dd>

Puntatore alle ore rimanenti.

</dd> <dt>

*pdwReserved* \[ out\]
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo ha esito positivo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





