---
description: Il metodo GetCurrentBuffer recupera una copia del buffer associato all'esempio più recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Metodo ISampleGrabber:: GetCurrentBuffer (qedit. h)'
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
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330509"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>Metodo ISampleGrabber:: GetCurrentBuffer

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **GetCurrentBuffer** recupera una copia del buffer associato all'esempio più recente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferSize* \[ in uscita\]
</dt> <dd>

Puntatore alla dimensione del buffer. Se *pbuffer* è **null**, questo parametro riceve le dimensioni del buffer richieste, in byte. Se *pbuffer* non è **null**, impostare questo parametro in modo che corrisponda alla dimensione del buffer, in byte. Nell'output il parametro riceve il numero di byte che sono stati copiati nel buffer. Questo valore può essere inferiore alla dimensione del buffer.

</dd> <dt>

*pbuffer* \[ out\]
</dt> <dd>

Puntatore a una matrice di byte di dimensioni *pBufferSize* o **null**. Se questo parametro non è **null**, il buffer corrente viene copiato nella matrice. Se questo parametro è **null**, il parametro *pBufferSize* riceve le dimensioni del buffer richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Gli esempi non vengono memorizzati nel buffer. Chiamare [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>         | Il buffer specificato non è sufficientemente grande.<br/>                                                                         |
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Argomento puntatore **null** .<br/>                                                                                        |
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il filtro non è connesso.<br/>                                                                                      |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl>   | Il filtro non ha ancora ricevuto esempi. Per recapitare un esempio, eseguire o sospendere il grafo.<br/>                         |



 

## <a name="remarks"></a>Commenti

Per attivare il buffering, chiamare [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**.

Chiamare questo metodo due volte. Alla prima chiamata, impostare *pbuffer* su **null**. La dimensione del buffer viene restituita in *pBufferSize*. Quindi allocare una matrice e chiamare di nuovo il metodo. Alla seconda chiamata, passare le dimensioni della matrice in *pBufferSize* e passare l'indirizzo della matrice in *pbuffer*. Se la matrice non è sufficientemente grande, il metodo restituisce E \_ OutOfMemory.

Il parametro *pbuffer* è tipizzato come puntatore **Long** , ma il contenuto del buffer dipende dal formato dei dati. Chiamare [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) per ottenere il tipo di supporto del formato.

Non chiamare questo metodo mentre è in esecuzione il grafico dei filtri. Durante l'esecuzione del grafico del filtro, il filtro Grabber di esempio sovrascrive il contenuto del buffer ogni volta che viene ricevuto un nuovo esempio. Il modo migliore per utilizzare questo metodo consiste nell'utilizzare la modalità "One-Shot", che interrompe il grafico dopo la ricezione del primo campione. Per impostare la modalità One-Shot, chiamare [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).

Il filtro non memorizza nel buffer gli esempi di preroll o gli esempi in cui il membro **dwStreamId** della struttura delle [**\_ \_ Proprietà SAMPLE2 di Am**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da quello dei flussi di dati \_ \_ .

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

 

 




