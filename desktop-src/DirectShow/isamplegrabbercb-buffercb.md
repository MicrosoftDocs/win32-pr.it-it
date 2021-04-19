---
description: Il metodo BufferCB è un metodo di callback che riceve un puntatore al buffer di esempio.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Metodo ISampleGrabberCB:: BufferCB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332640"
---
# <a name="isamplegrabbercbbuffercb-method"></a>Metodo ISampleGrabberCB:: BufferCB

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **BufferCB** è un metodo di callback che riceve un puntatore al buffer di esempio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SampleTime* 
</dt> <dd>

Ora di inizio dell'esempio, in secondi.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer che contiene i dati di esempio. Il formato dei dati dipende dal tipo di supporto del PIN di input del grabber di esempio. Per ottenere il tipo di supporto, chiamare [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*BufferLen* 
</dt> <dd>

Lunghezza del buffer a cui punta *pbuffer* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo di callback riceve un puntatore ai dati nell'esempio multimediale più recente.

> [!Note]  
> Questo metodo riceve un puntatore ai dati di esempio originali, non a una copia. La documentazione originale ha dichiarato erroneamente che *pbuffer* contiene una copia dei dati.

 

Per impostare il callback, chiamare [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md).

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

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




