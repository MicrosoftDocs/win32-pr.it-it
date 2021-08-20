---
description: Il metodo WriteBitmapBits recupera un fotogramma video all'ora del contenuto multimediale specificato e lo scrive in un file. Il fotogramma video è sempre in formato RGB a 24 bit.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: Metodo IMediaDet::WriteBitmapBits (Qedit.h)
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
ms.openlocfilehash: fc2a967f5b0e99c50317e9dc226a4b345c6790a8ce2b6e5d42eb50dfdc3b105b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154156"
---
# <a name="imediadetwritebitmapbits-method"></a>Metodo IMediaDet::WriteBitmapBits

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `WriteBitmapBits` metodo recupera un fotogramma video all'ora del contenuto multimediale specificato e lo scrive in un file. Il fotogramma video è sempre in formato RGB a 24 bit.

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

Ora in cui recuperare il fotogramma video.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'immagine, in pixel.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza dell'immagine, in pixel.

</dd> <dt>

*Filename* 
</dt> <dd>

Percorso del file in cui salvare la bitmap. Se il file esiste già, questo metodo lo sovrascrive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ L'operazione ha esito positivo. In caso contrario, restituisce **un valore HRESULT** che indica la causa dell'errore. I codici di errore possibili sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Impossibile aggiungere il [**filtro Sample Grabber**](sample-grabber-filter.md) al grafico.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                  | Esito negativo.<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insufficiente.<br/>                                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | Errore imprevisto.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | Impossibile sovrascrivere il file.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                                                    |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome file e il flusso chiamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream.**](imediadet-put-currentstream.md)

Questo metodo imposta il rilevatore multimediale in modalità di cattura bitmap. Dopo aver chiamato questo metodo, i vari metodi di informazioni di flusso in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevatore multimediale.

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

 

 




