---
description: Il metodo GetMuted recupera lo stato disattivato dell'oggetto.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: Metodo IAMTimelineObj::GetMuted (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f30c0292316f1c876216532b9a2a3193317370d0103ddbc0ab94c6801fae1504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051651"
---
# <a name="iamtimelineobjgetmuted-method"></a>Metodo IAMTimelineObj::GetMuted

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetMuted` metodo recupera lo stato disattivato dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pval* 
</dt> <dd>

Riceve un valore che indica lo stato disattivato. Se il valore è **TRUE,** l'oggetto e i relativi elementi figlio vengono disattivati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se l'elemento padre di un oggetto è disattivato, l'oggetto viene disattivato indipendentemente dallo stato disattivato. Quando l'elemento padre non viene più disattivato, viene ripristinato lo stato di disattivazione precedente dell'oggetto.

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

 

 




