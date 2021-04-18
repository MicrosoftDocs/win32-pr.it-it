---
description: Il metodo GetNextSrcEx recupera l'origine successiva dopo l'origine specificata.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Metodo IAMTimelineTrack:: GetNextSrcEx (qedit. h)'
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
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325636"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>Metodo IAMTimelineTrack:: GetNextSrcEx

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

*pLast* 
</dt> <dd>

Puntatore all'oggetto di origine precedente oppure **null** per recuperare la prima origine nella traccia.

</dd> <dt>

*ppNext* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine successivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.

## <a name="remarks"></a>Commenti

Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




