---
description: Il metodo SetCallback specifica un metodo di callback da chiamare sugli esempi in ingresso.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: Metodo ISampleGrabber::SetCallback (Qedit.h)
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
ms.openlocfilehash: 6e6d61d60a4664386cded025d2b7bcea82353602c7f7f8c0fb5bc4c53779ae2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817918"
---
# <a name="isamplegrabbersetcallback-method"></a>Metodo ISampleGrabber::SetCallback

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il **metodo SetCallback** specifica un metodo di callback da chiamare sugli esempi in ingresso.

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

Puntatore a [**un'interfaccia ISampleGrabberCB**](isamplegrabbercb.md) contenente il metodo di callback oppure **NULL per** annullare il callback.

</dd> <dt>

*Oggetto WhichMethodToCallback* 
</dt> <dd>

Indice che specifica il metodo di callback. Deve essere uno dei valori seguenti.



| Valore | Descrizione                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Il filtro Grabber di esempio chiama il [**metodo ISampleGrabberCB::SampleCB.**](isamplegrabbercb-samplecb.md) Questo metodo riceve un [**puntatore IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)               |
| 1     | Il filtro Grabber di esempio chiama il [**metodo ISampleGrabberCB::BufferCB.**](isamplegrabbercb-buffercb.md) Questo metodo riceve un puntatore al buffer contenuto nell'esempio multimediale. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il thread di elaborazione dati si blocca fino alla fine del metodo di callback. Se il callback non restituisce rapidamente, può interferire con la riproduzione.

Il filtro non richiama la funzione di callback per gli esempi di pre-registrazione o per gli esempi in cui il membro **dwStreamId** della struttura [**AM \_ SAMPLE2 \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da AM \_ STREAM \_ MEDIA.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di Grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




