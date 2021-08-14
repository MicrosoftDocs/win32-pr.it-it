---
description: Il metodo SetUserName imposta un nome definito dall'applicazione per l'oggetto.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: Metodo IAMTimelineObj::SetUserName (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0656428ad591372495170a6e7e688a593fe496e07d9f01e9dd3f348b9f527d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399666"
---
# <a name="iamtimelineobjsetusername-method"></a>Metodo IAMTimelineObj::SetUserName

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetUserName` metodo imposta un nome definito dall'applicazione per l'oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Stringa di caratteri wide che contiene il nome. Le stringhe di lunghezza superiore a 256 caratteri potrebbero essere troncate.

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

 

 




