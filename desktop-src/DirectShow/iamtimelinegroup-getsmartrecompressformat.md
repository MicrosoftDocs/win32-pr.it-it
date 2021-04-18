---
description: Il metodo GetSmartRecompressFormat Recupera il formato di compressione corrente per la ricompressione intelligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Metodo IAMTimelineGroup:: GetSmartRecompressFormat (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328618"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>Metodo IAMTimelineGroup:: GetSmartRecompressFormat

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSmartRecompressFormat` metodo recupera il formato di compressione corrente per la ricompressione intelligente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFormat* 
</dt> <dd>

Riceve un puntatore a una struttura [**SCompFmt0**](scompfmt0.md) , di cui viene eseguito il cast come puntatore a un oggetto Long. Se il metodo ha esito negativo, il valore viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se l'applicazione non ha impostato un formato di compressione intelligente (chiamando [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), il formato restituito da questo metodo non sarà valido. Chiamare il metodo [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) per determinare se è stato impostato un formato di compressione.

Se il metodo ha esito positivo, il chiamante deve liberare il tipo di supporto restituito ed eliminare la struttura [**SCompFmt0**](scompfmt0.md) :


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



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

 

 




