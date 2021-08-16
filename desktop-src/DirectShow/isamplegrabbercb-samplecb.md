---
description: Il metodo SampleCB è un metodo di callback che riceve un puntatore all'esempio multimediale.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: Metodo ISampleGrabberCB::SampleCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817513"
---
# <a name="isamplegrabbercbsamplecb-method"></a>Metodo ISampleGrabberCB::SampleCB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SampleCB` metodo è un metodo di callback che riceve un puntatore all'esempio multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SampleTime* 
</dt> <dd>

Ora di inizio dell'esempio, in secondi.

</dd> <dt>

*pSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore **HRESULT** in caso contrario.

## <a name="remarks"></a>Commenti

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

 

 




