---
description: Il metodo get \_ FrameRate recupera la frequenza dei fotogrammi del flusso corrente. Il flusso deve essere un flusso video.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: Metodo IMediaDet::get_FrameRate (Qedit.h)
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
ms.openlocfilehash: a22be2caf5a66447c9c772861918f1a5dcfe7bc2c81bfdba4f1fefb59f89565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154427"
---
# <a name="imediadetget_framerate-method"></a>Metodo IMediaDet::get \_ FrameRate

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_FrameRate` metodo recupera la frequenza dei fotogrammi del flusso corrente. Il flusso deve essere un flusso video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve la frequenza dei fotogrammi, in fotogrammi al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | L'intestazione del formato video non specifica una frequenza dei fotogrammi.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argomento non valido.<br/>                                  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>               | Argomento del puntatore **NULL.**<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                |



 

## <a name="remarks"></a>Commenti

Questo metodo non può recuperare la frequenza dei fotogrammi da un file ASF.

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

 

 




