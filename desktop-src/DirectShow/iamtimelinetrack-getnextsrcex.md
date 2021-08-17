---
description: Il metodo GetNextSrcEx recupera l'origine successiva dopo l'origine specificata.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: Metodo IAMTimelineTrack::GetNextSrcEx (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 438fcdbf4f95406994f5bf0cc63ebf5b5f600a9908419b63c4ceace65dfa9659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952800"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>Metodo IAMTimelineTrack::GetNextSrcEx

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetNextSrcEx` metodo recupera l'origine successiva dopo l'origine specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plast* 
</dt> <dd>

Puntatore all'oggetto di origine precedente oppure **NULL** per recuperare la prima origine nella traccia.

</dd> <dt>

*ppNext* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine successivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il metodo recupera un'origine oppure S FALSE in caso \_ contrario.

## <a name="remarks"></a>Commenti

Se il metodo restituisce S \_ OK, **l'interfaccia IAMTimelineObj** restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

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

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




