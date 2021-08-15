---
description: Il metodo RemoveAll rimuove definitivamente questo oggetto dalla sequenza temporale, inclusi gli oggetti secondari e gli elementi figlio.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: Metodo IAMTimelineObj::RemoveAll (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 92bae081c5f888d271bfdeb278ca4c0d2b210fffddce8b57c76d5f446fc9e4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400749"
---
# <a name="iamtimelineobjremoveall-method"></a>Metodo IAMTimelineObj::RemoveAll

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `RemoveAll` metodo rimuove definitivamente questo oggetto dalla sequenza temporale, inclusi gli oggetti secondari e gli elementi figlio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Per rimuovere un oggetto allo scopo di reinserirlo in un altro punto della sequenza temporale, chiamare [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).

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

 

 




