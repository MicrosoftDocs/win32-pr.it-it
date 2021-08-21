---
description: Il metodo get \_ StreamLength recupera la durata del flusso corrente.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: Metodo IMediaDet::get_StreamLength (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f29b11c5b9b054a759648343ea8b27c8f883d044cd65073b0bddc5ea8884a6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154288"
---
# <a name="imediadetget_streamlength-method"></a>Metodo IMediaDet::get \_ StreamLength

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_StreamLength` metodo recupera la durata del flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve la durata del flusso, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome file e il flusso chiamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream.**](imediadet-put-currentstream.md)

Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG. Per altre informazioni, vedere [**IMediaDet::EnterBitmapGrabMode.**](imediadet-enterbitmapgrabmode.md)

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




