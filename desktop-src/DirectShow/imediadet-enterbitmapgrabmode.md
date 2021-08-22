---
description: Il metodo EnterBitmapGrabMode passa il rilevatore multimediale alla modalità di cattura bitmap e cerca il grafico del filtro a un'ora specificata.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: Metodo IMediaDet::EnterBitmapGrabMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952620"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Metodo IMediaDet::EnterBitmapGrabMode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo passa il rilevatore multimediale alla modalità di cattura bitmap e cerca il grafico dei `EnterBitmapGrabMode` filtri a un'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StreamTime* 
</dt> <dd>

Tempo, in secondi, in base al quale viene cercato il grafico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argomento non valido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Il file di origine non ha un flusso video.<br/> |
| <dl> <dt>**VFW \_ E \_ TIME \_ EXPIRED**</dt> </dl>    | Timeout del comando Seek.<br/>                       |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome file e il flusso chiamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream.**](imediadet-put-currentstream.md)

Questo metodo inserisce il [**filtro Sample Grabber**](sample-grabber-filter.md) nel grafico dei filtri. È quindi possibile chiamare [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) per ottenere un puntatore [**all'interfaccia ISampleGrabber.**](isamplegrabber.md) Quando il rilevatore multimediale entra in modalità di cattura bitmap, i vari metodi in formato informativo in **IMediaDet** non funzionano.

I [**metodi IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) consentono anche di impostare il rilevatore multimediale in modalità di cattura bitmap.

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

 

 




