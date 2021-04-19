---
description: Il metodo IsNormalRate indica se la clip viene riprodotto alla frequenza di riproduzione normale; ovvero la velocità di riproduzione del file originale.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Metodo IAMTimelineSrc:: IsNormalRate (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332752"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>Metodo IAMTimelineSrc:: IsNormalRate

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `IsNormalRate` metodo indica se il clip verrà riprodotto alla frequenza di riproduzione normale, ovvero la velocità di riproduzione del file originale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve un valore booleano che indica come viene eseguito il rendering della clip. Se il valore è **true**, il clip verrà riprodotto alla tariffa normale. In caso contrario, verrà riprodotto più veloce o più lento del normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La velocità di riproduzione di una clip è determinata dalle ore di inizio e di fine del supporto, in relazione ai tempi di sequenza temporale:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Se questo rapporto è uguale a 1, il clip viene riprodotto alla velocità creata. In caso contrario, viene riprodotto più velocemente o più lentamente. Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




