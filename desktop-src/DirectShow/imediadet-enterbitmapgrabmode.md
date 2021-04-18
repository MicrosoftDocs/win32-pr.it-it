---
description: Il metodo EnterBitmapGrabMode passa il rilevatore di supporti alla modalità di recupero bitmap e cerca il grafico del filtro a un orario specificato.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Metodo IMediaDet:: EnterBitmapGrabMode (qedit. h)'
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
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328330"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Metodo IMediaDet:: EnterBitmapGrabMode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `EnterBitmapGrabMode` metodo passa il rilevatore di supporti alla modalità di recupero bitmap e cerca il grafico del filtro a un orario specificato.

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

Tempo, in secondi, in cui il grafico Cerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argomento non valido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Il file di origine non dispone di un flusso video.<br/> |
| <dl> <dt>**tempo di VFW \_ E \_ \_ scaduto**</dt> </dl>    | Timeout del comando seek.<br/>                       |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Questo metodo inserisce il filtro [**grabber di esempio**](sample-grabber-filter.md) nel grafico del filtro. È quindi possibile chiamare [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) per ottenere un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) . Quando il rilevamento multimediale passa alla modalità di cattura della bitmap, i vari metodi informativi in **IMediaDet** non funzionano.

I metodi [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) inseriscono anche il rilevatore multimediale in modalità di cattura bitmap.

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

 

 




