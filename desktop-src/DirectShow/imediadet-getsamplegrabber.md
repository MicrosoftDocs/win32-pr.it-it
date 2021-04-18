---
description: Il metodo GetSampleGrabber recupera un puntatore all'interfaccia ISampleGrabber, che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Metodo IMediaDet:: GetSampleGrabber (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327825"
---
# <a name="imediadetgetsamplegrabber-method"></a>Metodo IMediaDet:: GetSampleGrabber

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSampleGrabber` metodo recupera un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) , che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVal* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) prima di chiamare questo metodo. L'interfaccia [**ISampleGrabber**](isamplegrabber.md) consente di recuperare singoli esempi di supporti dal flusso. Se è sufficiente una bitmap da un fotogramma video, chiamare invece il metodo [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) . L'interfaccia **ISampleGrabber** è più flessibile, ma richiede più lavoro da parte dell'applicazione.

Se questo metodo ha esito positivo, l'interfaccia [**ISampleGrabber**](isamplegrabber.md) restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




