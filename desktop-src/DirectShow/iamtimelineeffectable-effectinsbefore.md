---
description: Il metodo EffectInsBefore inserisce un effetto nell'oggetto al livello di priorità specificato.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: Metodo IAMTimelineEffectable::EffectInsBefore (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0eca93a6c1837b8a7a8f5a95a6cdbf9e87f99191c0911a82e6fd7a3586eb8c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052751"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Metodo IAMTimelineEffectable::EffectInsBefore

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `EffectInsBefore` metodo inserisce un effetto nell'oggetto al livello di priorità specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFX* 
</dt> <dd>

Puntatore [**all'interfaccia IAMTimelineObj**](iamtimelineobj.md) dell'effetto.

</dd> <dt>

*Priorità* 
</dt> <dd>

Livello di priorità in corrispondenza del quale inserire l'effetto. Usare il valore –1 per inserire l'effetto alla fine dell'elenco di priorità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se ha esito positivo o E \_ NOTIMPL se l'oggetto non è un effetto. In caso contrario, restituisce un **altro valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Se necessario, i tempi di inizio e arresto dell'effetto vengono ritagliati entro i limiti dell'intervallo di tempo dell'oggetto. Se esiste già un effetto al livello di priorità specificato, tutti gli effetti da quel punto in poi spostano verso il basso l'elenco di priorità per fare spazio al nuovo effetto.

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

[**Interfaccia IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




