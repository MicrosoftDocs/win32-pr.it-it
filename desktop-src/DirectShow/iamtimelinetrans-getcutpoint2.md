---
description: Il metodo GetCutPoint2 recupera il punto di taglio. Questo metodo equivale a IAMTimelineTrans::GetCutPoint, ma accetta un valore REFTIME.
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: Metodo IAMTimelineTrans::GetCutPoint2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 291aff15260d5d693f3e6b0281d693a7351132fc017358f6f9ee21020dfd4f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952760"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a>Metodo IAMTimelineTrans::GetCutPoint2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetCutPoint2` metodo recupera il punto di taglio. Questo metodo equivale a [**IAMTimelineTrans::GetCutPoint,**](iamtimelinetrans-getcutpoint.md)ma accetta un [**valore REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTLTime* 
</dt> <dd>

Riceve il punto di taglio, in secondi, rispetto all'ora di inizio della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                               | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il punto di taglio non è stato impostato. Il valore restituito è il valore predefinito.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il punto di taglio è stato impostato su un valore diverso da quello predefinito.<br/>            |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl> | Argomento del puntatore **NULL.**<br/>                                          |



 

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




