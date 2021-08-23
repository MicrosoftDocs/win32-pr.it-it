---
description: Il metodo SetDefaultTransition imposta la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: Metodo IAMTimeline::SetDefaultTransition (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9271e922fe33865feb36b361ae97bb16298b504fb6cbb14066fbd6976c8065e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812411"
---
# <a name="iamtimelinesetdefaulttransition-method"></a>Metodo IAMTimeline::SetDefaultTransition

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetDefaultTransition` metodo imposta la transizione predefinita. Se il motore di rendering non è in grado di eseguire il rendering di una transizione, sostituisce la transizione predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a una variabile che contiene il GUID della transizione predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se non si imposta una transizione predefinita o se la transizione specificata come predefinita causa un errore, DES usa la propria transizione predefinita.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




