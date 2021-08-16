---
description: Il metodo GetCurrentBuffer recupera una copia del buffer associato all'esempio più recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: Metodo ISampleGrabber::GetCurrentBuffer (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88af9469a1470a02be62b7684a66990c5622820e370518ed53267bd87d981879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818050"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>Metodo ISampleGrabber::GetCurrentBuffer

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il **metodo GetCurrentBuffer** recupera una copia del buffer associato all'esempio più recente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferSize* \[ in, out\]
</dt> <dd>

Puntatore alle dimensioni del buffer. Se *pBuffer* è **NULL,** questo parametro riceve le dimensioni del buffer richieste, in byte. Se *pBuffer* non è **NULL,** impostare questo parametro sulla dimensione del buffer, in byte. Nell'output, il parametro riceve il numero di byte copiati nel buffer. Questo valore potrebbe essere minore delle dimensioni del buffer.

</dd> <dt>

*pBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di byte di dimensioni *pBufferSize* o **NULL.** Se questo parametro non è **NULL,** il buffer corrente viene copiato nella matrice. Se questo parametro è **NULL,** il *parametro pBufferSize* riceve le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Gli esempi non vengono memorizzati nel buffer. Chiamare [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Il buffer specificato non è sufficientemente grande.<br/>                                                                         |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il filtro non è connesso.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl>   | Il filtro non ha ancora ricevuto alcun esempio. Per distribuire un esempio, eseguire o sospendere il grafo.<br/>                         |



 

## <a name="remarks"></a>Commenti

Per attivare il buffering, chiamare [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con valore **TRUE.**

Chiamare questo metodo due volte. Nella prima chiamata impostare *pBuffer* su **NULL.** Le dimensioni del buffer vengono restituite in *pBufferSize*. Allocare quindi una matrice e chiamare nuovamente il metodo . Nella seconda chiamata, passare le dimensioni della matrice in *pBufferSize* e passare l'indirizzo della matrice in *pBuffer*. Se la matrice non è sufficientemente grande, il metodo restituisce E \_ OUTOFMEMORY.

Il *parametro pBuffer* è tipiato come **puntatore long,** ma il contenuto del buffer dipende dal formato dei dati. Chiamare [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) per ottenere il tipo di supporto del formato.

Non chiamare questo metodo durante l'esecuzione del grafico dei filtri. Mentre il grafico dei filtri è in esecuzione, il filtro Grabber di esempio sovrascrive il contenuto del buffer ogni volta che riceve un nuovo campione. Il modo migliore per usare questo metodo è usare la "modalità one-shot", che arresta il grafo dopo la ricezione del primo esempio. Per impostare la modalità one-shot, chiamare [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).

Il filtro non esegue il buffer degli esempi di pre-registrazione o degli esempi in cui il membro **dwStreamId** della struttura [**\_ AM SAMPLE2 \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da AM \_ STREAM \_ MEDIA.

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

 

 




