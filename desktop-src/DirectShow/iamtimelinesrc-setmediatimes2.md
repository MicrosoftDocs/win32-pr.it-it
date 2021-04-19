---
description: "Il metodo SetMediaTimes2 imposta l'ora di inizio e di fine del supporto. Questo metodo è equivalente a IAMTimelineSrc:: SetMediaTimes, ma accetta valori REFTIME."
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Metodo IAMTimelineSrc:: SetMediaTimes2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332747"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a>Metodo IAMTimelineSrc:: SetMediaTimes2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaTimes2` metodo imposta l'ora di inizio e di fine del supporto. Questo metodo è equivalente a [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md), ma accetta valori [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

Ora di inizio del supporto, in secondi.

</dd> <dt>

*Stop* 
</dt> <dd>

Tempo di arresto del supporto, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

 

 




