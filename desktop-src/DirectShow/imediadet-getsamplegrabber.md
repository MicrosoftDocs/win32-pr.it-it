---
description: Il metodo GetSampleGrabber recupera un puntatore all'interfaccia ISampleGrabber, che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: Metodo IMediaDet::GetSampleGrabber (Qedit.h)
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
ms.openlocfilehash: f2c3c580a44b9cff35d7ee801cfc611b5cf8a8df828f54c28b022e5c1a1b862a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819043"
---
# <a name="imediadetgetsamplegrabber-method"></a>Metodo IMediaDet::GetSampleGrabber

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetSampleGrabber` metodo recupera un puntatore all'interfaccia [**ISampleGrabber,**](isamplegrabber.md) che consente a un'applicazione di recuperare singoli campioni da un flusso multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVal* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia ISampleGrabber.**](isamplegrabber.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Chiamare [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) prima di chiamare questo metodo. [**L'interfaccia ISampleGrabber**](isamplegrabber.md) consente di recuperare singoli campioni multimediali dal flusso. Se è necessaria solo una bitmap da un fotogramma video, chiamare invece il metodo [**IMediaDet::GetBitmapBits.**](imediadet-getbitmapbits.md) **L'interfaccia ISampleGrabber** è più flessibile, ma richiede più lavoro da parte dell'applicazione.

Se questo metodo ha esito positivo, [**l'interfaccia ISampleGrabber**](isamplegrabber.md) restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

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

 

 




