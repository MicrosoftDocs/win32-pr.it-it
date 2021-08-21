---
description: Il metodo GetStartStop2 recupera gli orari di inizio e arresto dell'oggetto, rispetto all'elemento padre dell'oggetto. Questo metodo equivale a IAMTimelineObj::GetStartStop, ma accetta valori REFTIME.
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: Metodo IAMTimelineObj::GetStartStop2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ff1644c2ba83848d0c9efa1b850a65aa8cfd1de1607a9fa0cabbab39579e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155452"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>Metodo IAMTimelineObj::GetStartStop2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera le ore di inizio e arresto `GetStartStop2` dell'oggetto, rispetto all'elemento padre dell'oggetto. Questo metodo equivale a [**IAMTimelineObj::GetStartStop,**](iamtimelineobj-getstartstop.md)ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Riceve l'ora di inizio, in secondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve l'ora di arresto, in secondi.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




