---
description: Il metodo SetOneShot specifica se il filtro Grabber di esempio si interrompe dopo che il filtro riceve un campione.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Metodo ISampleGrabber:: SetOneShot (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327664"
---
# <a name="isamplegrabbersetoneshot-method"></a>Metodo ISampleGrabber:: SetOneShot

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **SetOneShot** specifica se il filtro [**grabber di esempio**](sample-grabber-filter.md) si interrompe dopo che il filtro riceve un campione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OneShot* 
</dt> <dd>

Valore booleano che specifica se il filtro Grabber di esempio si arresta dopo la ricezione di un campione.



| Valore                                                                                                                                    | Significato                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Il grabber di esempio si arresta dopo il primo campione. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Dopo il primo esempio, il grabber di esempio continua a elaborare gli esempi. Comportamento predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Usare questo metodo per ottenere un singolo campione dal flusso, come indicato di seguito:

1.  Chiamare **SetOneShot** con il valore **true**.
2.  Facoltativamente, usare l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) per cercare una posizione nel flusso.
3.  Chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico del filtro.
4.  Chiamare [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) per attendere che il grafico si interrompa. In alternativa, chiamare [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere gli eventi del grafo, fino a quando non si riceve l'evento di [**\_ completamento EC**](ec-complete.md) .

Dopo l'arresto di Sample grabber, il grafico del filtro è ancora in stato di esecuzione. È possibile cercare o sospendere il grafo per ottenere un altro esempio.

> [!Note]  
> Una versione precedente della documentazione ha dichiarato che il grafico di filtro si interrompe dopo la ricezione dell'esempio. Questo non è accurato. Il flusso termina, ma il grafo rimane nello stato in esecuzione.

 

Il grabber di esempio implementa la modalità One-Shot chiamando [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul filtro downstream e restituendo \_ false dal metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

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

 

 




