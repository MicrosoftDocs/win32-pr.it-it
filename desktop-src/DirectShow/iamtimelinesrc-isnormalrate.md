---
description: Il metodo IsNormalRate indica se il clip verrà riprodotto alla velocità di riproduzione normale. cio, la velocità di riproduzione del file originale.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: Metodo IAMTimelineSrc::IsNormalRate (Qedit.h)
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
ms.openlocfilehash: 4d1c0b355b0eedee29dafb92debbabac5c7b3e574d2f161827626bc73f72c035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083871"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>Metodo IAMTimelineSrc::IsNormalRate

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo indica se il clip verrà riprodotto alla velocità di riproduzione normale, cio' la velocità di `IsNormalRate` riproduzione del file originale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pval* 
</dt> <dd>

Riceve un valore booleano che indica come verrà eseguito il rendering del clip. Se il valore è **TRUE,** il clip verrà riprodotto alla velocità normale. In caso contrario, verrà riprodotto più velocemente o più lento del normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

La velocità di riproduzione di un clip è determinata dai relativi tempi di avvio e arresto dei supporti, in relazione agli orari della sequenza temporale:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Se questo rapporto è uguale a 1, il clip viene riprodotto alla velocità di creazione. In caso contrario, viene riprodotto più velocemente o più lento. Per altre informazioni, vedere [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




