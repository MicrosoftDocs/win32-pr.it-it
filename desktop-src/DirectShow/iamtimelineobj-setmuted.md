---
description: Il metodo semutato imposta lo stato di disattivazione dell'oggetto. Un oggetto disattivato non viene sottoposto a rendering, ma rimane nella sequenza temporale.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Metodo IAMTimelineObj:: tomute (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330816"
---
# <a name="iamtimelineobjsetmuted-method"></a>Metodo IAMTimelineObj:: tomute

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMuted` metodo imposta lo stato di disattivazione dell'oggetto. Un oggetto disattivato non viene sottoposto a rendering, ma rimane nella sequenza temporale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Flag che specifica lo stato disattivato. Se **true**, l'oggetto e tutti i relativi elementi figlio sono disabilitati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il muting di un oggetto disattiva anche gli elementi figlio contenuti nell'oggetto. Se, ad esempio, si disattiva una traccia, anche le transizioni, le origini e gli effetti di tale traccia vengono disabilitati. Quando l'oggetto non viene più disattivato, i relativi elementi figlio ripristinano lo stato precedente, che potrebbe essere disattivato o non disattivato.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




