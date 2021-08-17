---
description: Il metodo VTrackSwapPriorities cambia i livelli di priorità di due tracce.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: Metodo IAMTimelineComp::VTrackSwapPriorities (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eb67e07f96ec2e8377690a5cd5233ba6cdb40242870da6d5f23b5f404b77b890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999284"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>Metodo IAMTimelineComp::VTrackSwapPriorities

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `VTrackSwapPriorities` metodo cambia i livelli di priorità di due tracce.

Dati due livelli di priorità, questo metodo cambia le tracce virtuali in base a tali priorità. Quando il metodo viene restituito, la traccia che si trova al primo livello di priorità è ora al secondo livello di priorità e viceversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Primo livello di priorità al quale scambiare le tracce virtuali.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Secondo livello di priorità al quale scambiare le tracce virtuali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




