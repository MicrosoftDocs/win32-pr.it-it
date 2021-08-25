---
description: Il metodo GetStartStop recupera gli orari di inizio e arresto dell'oggetto, rispetto all'elemento padre dell'oggetto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: Metodo IAMTimelineObj::GetStartStop (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400787"
---
# <a name="iamtimelineobjgetstartstop-method"></a>Metodo IAMTimelineObj::GetStartStop

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera le ore di inizio e arresto `GetStartStop` dell'oggetto, rispetto all'elemento padre dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Riceve l'ora di inizio, in unità da 100 nanosecondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve l'ora di arresto, in unità da 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le composizioni, i gruppi e le tracce hanno sempre un'ora di inizio 0.

Durante il rendering, DES arrotonda i tempi di inizio e arresto di un oggetto al limite del frame più vicino. Des, tuttavia, non sovrascrive gli orari dell'oggetto. Se si modifica la frequenza fotogrammi del gruppo, gli orari arrotondati vengono sempre calcolati a partire dall'ora originale. Per altre informazioni, [vedere Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Per determinare l'ora di inizio e di arresto nel progetto sottoposto a rendering, passare i valori restituiti da al metodo `GetStartStop` [**IAMTimelineObj::FixTimes.**](iamtimelineobj-fixtimes.md)

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

 

 




