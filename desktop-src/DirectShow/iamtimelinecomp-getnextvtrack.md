---
description: Il metodo GetNextVTrack recupera la traccia virtuale successiva dopo una traccia virtuale specificata.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: Metodo IAMTimelineComp::GetNextVTrack (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dbeaf5d7987f1baf2b3df9804c4abd3049c38042a29f4177f83abec6855140a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401052"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>Metodo IAMTimelineComp::GetNextVTrack

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetNextVTrack` metodo recupera la traccia virtuale successiva dopo una traccia virtuale specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Puntatore alla traccia virtuale precedente oppure **NULL per** recuperare la prima traccia virtuale nella composizione.

</dd> <dt>

*ppNextVirtualTrack* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale successiva, in ordine di priorità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK se il metodo recupera una traccia virtuale oppure S FALSE in \_ \_ caso contrario.

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, **l'interfaccia IAMTimelineObj** restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




