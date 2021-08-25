---
description: Il metodo SetMediaTypeForVB specifica il tipo di supporto del gruppo, per i client di Automazione.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: Metodo IAMTimelineGroup::SetMediaTypeForVB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ea47e4edcdfc58e38e61a9f92eb5afac0092ab0cb445f6ff73471e1b65b1480b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905041"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Metodo IAMTimelineGroup::SetMediaTypeForVB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetMediaTypeForVB` metodo specifica il tipo di supporto del gruppo, per i client di Automazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* \[ Pollici\]
</dt> <dd>

Valore che specifica il tipo di supporto. Impostare il valore su 0 per il video o su 1 per l'audio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo è destinato ai client di automazione. Per le applicazioni C++, usare il [**metodo IAMTimelineGroup::SetMediaType.**](iamtimelinegroup-setmediatype.md)

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




