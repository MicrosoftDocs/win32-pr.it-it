---
description: Il metodo SetUserID imposta un identificatore definito dall'applicazione per l'oggetto .
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: Metodo IAMTimelineObj::SetUserID (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a4c04f2e401778d65e661e56ce546263764adfda7063308ac9b9a5a85e12bda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078961"
---
# <a name="iamtimelineobjsetuserid-method"></a>Metodo IAMTimelineObj::SetUserID

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetUserID` metodo imposta un identificatore definito dall'applicazione per l'oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Valore che specifica l'identificatore. Questo identificatore viene usato solo dall'applicazione e può essere qualsiasi valore.

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

 

 




