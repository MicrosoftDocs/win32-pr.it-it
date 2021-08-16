---
description: Il metodo SetBufferSamples specifica se copiare i dati di esempio in un buffer mentre passano attraverso il filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: Metodo ISampleGrabber::SetBufferSamples (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817996"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Metodo ISampleGrabber::SetBufferSamples

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il **metodo SetBufferSamples** specifica se copiare i dati di esempio in un buffer mentre passano attraverso il filtro.

## <a name="syntax"></a>Sintassi


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BufferThem* 
</dt> <dd>

Valore booleano che specifica se i dati di esempio devono essere memorizzati nel buffer. Se **TRUE,** il filtro copia i dati di esempio in un buffer interno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per ottenere il buffer copiato, chiamare [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).

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

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




