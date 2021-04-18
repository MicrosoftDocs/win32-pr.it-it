---
description: Il metodo SetOutputBuffering specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Metodo IAMTimelineGroup:: SetOutputBuffering (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331628"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>Metodo IAMTimelineGroup:: SetOutputBuffering

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetOutputBuffering` metodo specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nBuffer* \[ in\]
</dt> <dd>

Numero di frame da memorizzare nel buffer durante l'anteprima. Deve essere maggiore o uguale a due.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Un buffer più grande richiede più memoria, ma può comportare una visualizzazione in anteprima più uniforme, soprattutto durante gli effetti o le transizioni che richiedono più tempo per il rendering. Il buffer predefinito è 30 fotogrammi.

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




