---
description: Il metodo SetMediaLength specifica la durata del file di origine.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Metodo IAMTimelineSrc:: SetMediaLength (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332749"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>Metodo IAMTimelineSrc:: SetMediaLength

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaLength` metodo specifica la durata del file di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Length* 
</dt> <dd>

Lunghezza del supporto, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

È possibile evitare potenziali errori di rendering impostando la lunghezza del supporto prima di impostare l'ora di arresto del supporto. Quando si imposta l'ora di arresto del supporto, DES verifica la lunghezza del supporto.

Questo metodo non convalida il parametro *length* , ma il valore deve corrispondere alla durata effettiva del file di origine. Ottenere la durata del file di origine chiamando [**IMediaDet:: Get \_ StreamLength**](imediadet-get-streamlength.md).

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

 

 




