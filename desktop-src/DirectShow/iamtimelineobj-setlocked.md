---
description: Il metodo SetLocked imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: Metodo IAMTimelineObj::SetLocked (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 87298b4e1fe9bc821c72d46d09d55e898b453292940029b7189a92e455b4c206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052481"
---
# <a name="iamtimelineobjsetlocked-method"></a>Metodo IAMTimelineObj::SetLocked

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetLocked` metodo imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.

Uno stato bloccato indica che l'oggetto non deve essere modificato. Uno stato sbloccato indica che l'oggetto può essere modificato. La sequenza temporale non applica il blocco. L'impostazione di blocco esiste solo per comodità dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Valore booleano che specifica lo stato di modifica dell'oggetto. Se **TRUE,** l'oggetto è bloccato e non deve essere modificato. Se **FALSE,** l'oggetto è sbloccato e può essere modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




