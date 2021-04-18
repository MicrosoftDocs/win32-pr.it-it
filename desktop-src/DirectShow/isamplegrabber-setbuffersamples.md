---
description: Il metodo SetBufferSamples specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Metodo ISampleGrabber:: SetBufferSamples (qedit. h)'
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
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330504"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Metodo ISampleGrabber:: SetBufferSamples

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **SetBufferSamples** specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.

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

Valore booleano che specifica se memorizzare nel buffer i dati di esempio. Se **true**, il filtro copia i dati di esempio in un buffer interno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per ottenere il buffer copiato, chiamare [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).

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

 

 




