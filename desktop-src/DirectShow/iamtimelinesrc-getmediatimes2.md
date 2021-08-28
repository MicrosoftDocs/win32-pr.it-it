---
description: Il metodo GetMediaTimes2 recupera le ore di avvio e arresto dei supporti. Questo metodo equivale a IAMTimelineSrc::GetMediaTimes, ma accetta valori REFTIME.
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: Metodo IAMTimelineSrc::GetMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3074cb0d416769e8e40f2f77814ac5603536df162e8d8a50fd2e916cfdc8931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052311"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a>Metodo IAMTimelineSrc::GetMediaTimes2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetMediaTimes2` metodo recupera i tempi di avvio e arresto dei supporti. Questo metodo equivale a [**IAMTimelineSrc::GetMediaTimes,**](iamtimelinesrc-getmediatimes.md)ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Riceve l'ora di inizio del supporto, in secondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve il tempo di arresto del supporto, espresso in secondi.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




