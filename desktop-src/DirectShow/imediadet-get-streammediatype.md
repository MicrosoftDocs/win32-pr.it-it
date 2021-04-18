---
description: Il \_ metodo Get StreamMediaType Recupera il tipo di supporto del flusso corrente. Tutti i flussi video vengono convertiti in tipi VIDEOINFOHEADER e tutti i flussi audio vengono convertiti in tipi WAVEFORMATEX.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Metodo IMediaDet:: get_StreamMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331501"
---
# <a name="imediadetget_streammediatype-method"></a>Metodo IMediaDet:: Get \_ StreamMediaType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_StreamMediaType` metodo recupera il tipo di supporto del flusso corrente. Tutti i flussi video vengono convertiti in tipi [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e tutti i flussi audio vengono convertiti in tipi [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) compilata con il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

 

 
