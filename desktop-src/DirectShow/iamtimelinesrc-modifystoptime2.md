---
description: Il metodo ModifyStopTime2 imposta l'ora di arresto. Questo metodo equivale a IAMTimelineSrc::ModifyStopTime, ma accetta un valore REFTIME.
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: Metodo IAMTimelineSrc::ModifyStopTime2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa2ec7a019200f91c9fb2a894c978ce93896926024f55efb229c7e5fde6fbe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952810"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Metodo IAMTimelineSrc::ModifyStopTime2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `ModifyStopTime2` metodo imposta l'ora di arresto. Questo metodo equivale a [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), ma accetta un [**valore REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stop* 
</dt> <dd>

Nuovo tempo di arresto, espresso in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure E \_ INVALIDARG se l'ora specificata non è valida.

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




