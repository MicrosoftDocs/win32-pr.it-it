---
description: Il metodo BufferCB è un metodo di callback che riceve un puntatore al buffer di esempio.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: Metodo ISampleGrabberCB::BufferCB (Qedit.h)
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
ms.openlocfilehash: c92e83c8daf5bf129a9aa8330bcc53caa88537f2395aeceebd8b5da2037c5b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817591"
---
# <a name="isamplegrabbercbbuffercb-method"></a>Metodo ISampleGrabberCB::BufferCB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il **metodo BufferCB** è un metodo di callback che riceve un puntatore al buffer di esempio.

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

Puntatore a un buffer che contiene i dati di esempio. Il formato dei dati dipende dal tipo di supporto del pin di input di Sample Grabber. Per ottenere il tipo di supporto, chiamare [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*BufferLen* 
</dt> <dd>

Lunghezza in byte del buffer a cui *punta pBuffer.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore **HRESULT** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo di callback riceve un puntatore ai dati nell'esempio multimediale più recente.

> [!Note]  
> Questo metodo riceve un puntatore ai dati di esempio originali, non una copia. La documentazione originale ha erroneamente dichiarato *che pBuffer* contiene una copia dei dati.

 

Per configurare il callback, chiamare [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).

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

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




