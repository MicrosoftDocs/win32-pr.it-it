---
description: Il metodo TransAdd aggiunge una transizione all'oggetto . Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo. Le transizioni devono rientrare nei limiti di tempo dell'oggetto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: Metodo IAMTimelineTransable::TransAdd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 930c3ff43e11cfb71ffce6c7257d0124fe87aeaaf4ae065433f11b860020eeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952750"
---
# <a name="iamtimelinetransabletransadd-method"></a>Metodo IAMTimelineTransable::TransAdd

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `TransAdd` metodo aggiunge una transizione all'oggetto . Un oggetto può avere più transizioni, ma non devono sovrapporsi nel tempo. Le transizioni devono rientrare nei limiti di tempo dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTrans* 
</dt> <dd>

Puntatore [**all'interfaccia IAMTimelineObj**](iamtimelineobj.md) della transizione da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                   | Descrizione                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Impossibile inserire la transizione.<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *pTrans* non è un puntatore a una transizione.<br/> |



 

## <a name="remarks"></a>Commenti

Se la transizione si sovrappone a una transizione esistente, il metodo restituisce E \_ INVALIDARG.

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

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




