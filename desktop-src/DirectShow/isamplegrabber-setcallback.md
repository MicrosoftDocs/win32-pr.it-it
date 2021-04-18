---
description: Il metodo di callback specifica un metodo di callback da chiamare sugli esempi in arrivo.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Metodo ISampleGrabber:: secallback (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330505"
---
# <a name="isamplegrabbersetcallback-method"></a>Metodo ISampleGrabber:: secallback

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il **metodo di callback specifica** un metodo di callback da chiamare sugli esempi in arrivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallback* 
</dt> <dd>

Puntatore a un'interfaccia [**ISampleGrabberCB**](isamplegrabbercb.md) contenente il metodo di callback o **null** per annullare il callback.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Indice che specifica il metodo di callback. Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Il filtro Grabber di esempio chiama il metodo [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) . Questo metodo riceve un puntatore [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .               |
| 1     | Il filtro Grabber di esempio chiama il metodo [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) . Questo metodo riceve un puntatore al buffer contenuto nell'esempio multimediale. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il thread di elaborazione dati si blocca fino a quando il metodo di callback non viene restituito. Se il callback non viene restituito rapidamente, può interferire con la riproduzione.

Il filtro non richiama la funzione di callback per gli esempi di preroll o per gli esempi in cui il membro **dwStreamId** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da quello dei flussi di dati am \_ \_ .

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

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




