---
description: Il metodo SetOneShot specifica se il filtro Grabber di esempio si arresta dopo la ricezione di un campione da parte del filtro.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: Metodo ISampleGrabber::SetOneShot (Qedit.h)
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
ms.openlocfilehash: 7829bd57cb2d813f71e17a4925d6e5fab7cc34330041461b691e00eae6ca5cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817682"
---
# <a name="isamplegrabbersetoneshot-method"></a>Metodo ISampleGrabber::SetOneShot

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il **metodo SetOneShot** specifica se il filtro [**Grabber**](sample-grabber-filter.md) di esempio si arresta dopo la ricezione di un campione da parte del filtro.

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
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Il grabber di esempio si arresta dopo il primo esempio. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Dopo il primo esempio, Sample Grabber continua a elaborare gli esempi. Comportamento predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare questo metodo per ottenere un singolo esempio dal flusso, come indicato di seguito:

1.  Chiamare **SetOneShot** con il valore **TRUE.**
2.  Facoltativamente, usare [**l'interfaccia IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) per cercare una posizione nel flusso.
3.  Chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico dei filtri.
4.  Chiamare [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) per attendere l'arresto del grafo. In alternativa, chiamare [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere gli eventi del grafo, fino a quando non si riceve [**l'evento EC \_ COMPLETE.**](ec-complete.md)

Dopo l'arresto di Sample Grabber, il grafico dei filtri è ancora in esecuzione. È possibile cercare o sospendere il grafo per ottenere un altro esempio.

> [!Note]  
> Una versione precedente della documentazione ha dichiarato che il grafo del filtro si arresta dopo la ricezione dell'esempio. Questo non è accurato. Il flusso termina, ma il grafico rimane in esecuzione.

 

L'esempio Grabber implementa la modalità one-shot chiamando [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul filtro downstream e restituisce S FALSE dal metodo \_ [**IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

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

 

 




