---
description: Il \_ metodo Get framerate recupera la frequenza dei fotogrammi del flusso corrente. Il flusso deve essere un flusso video.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Metodo IMediaDet:: get_FrameRate (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331505"
---
# <a name="imediadetget_framerate-method"></a>Metodo IMediaDet:: Get \_ framerate

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_FrameRate` metodo recupera la frequenza dei fotogrammi del flusso corrente. Il flusso deve essere un flusso video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve la frequenza dei fotogrammi, in frame al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                 | L'intestazione del formato video non specifica una frequenza dei fotogrammi.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argomento non valido.<br/>                                  |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                |



 

## <a name="remarks"></a>Commenti

Questo metodo non è in grado di recuperare la frequenza dei fotogrammi da un file ASF.

Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG. Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




