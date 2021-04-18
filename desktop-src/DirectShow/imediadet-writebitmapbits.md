---
description: Il metodo WriteBitmapBits recupera un frame video nel tempo di supporto specificato e lo scrive in un file. Il fotogramma video è sempre in formato RGB a 24 bit.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Metodo IMediaDet:: WriteBitmapBits (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327821"
---
# <a name="imediadetwritebitmapbits-method"></a>Metodo IMediaDet:: WriteBitmapBits

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `WriteBitmapBits` metodo recupera un frame video nel tempo di supporto specificato e lo scrive in un file. Il fotogramma video è sempre in formato RGB a 24 bit.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StreamTime* 
</dt> <dd>

Ora in cui recuperare il frame del video.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'immagine in pixel.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza, in pixel, dell'immagine.

</dd> <dt>

*Filename* 
</dt> <dd>

Percorso del file in cui salvare la bitmap. Se il file esiste già, questo metodo lo sovrascrive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK. l'operazione è riuscita. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore. I codici di errore possibili includono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | Non è stato possibile aggiungere il filtro [**grabber di esempio**](sample-grabber-filter.md) al grafo.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                  | Esito negativo.<br/>                                                                               |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>           | Memoria insufficiente.<br/>                                                                   |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>            | Errore imprevisto.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ AccessDenied**</dt> </dl>     | Impossibile sovrascrivere il file.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                                                    |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Questo metodo inserisce il rilevatore multimediale in modalità di cattura bitmap. Una volta che questo metodo è stato chiamato, i vari metodi di informazioni sui flussi in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevamento multimediale.

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

 

 




