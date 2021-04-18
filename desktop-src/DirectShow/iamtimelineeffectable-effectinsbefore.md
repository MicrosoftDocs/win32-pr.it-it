---
description: Il metodo EffectInsBefore inserisce un effetto nell'oggetto al livello di priorità specificato.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Metodo IAMTimelineEffectable:: EffectInsBefore (qedit. h)'
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
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333697"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Metodo IAMTimelineEffectable:: EffectInsBefore

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

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

Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'effetto.

</dd> <dt>

*Priorità* 
</dt> <dd>

Livello di priorità in corrispondenza del quale inserire l'effetto. Usare il valore-1 per inserire l'effetto alla fine dell'elenco di priorità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o E \_ NOTIMPL se l'oggetto non è un effetto. In caso contrario, restituisce un altro valore **HRESULT** che indica la cause dell'errore.

## <a name="remarks"></a>Commenti

Se necessario, le ore di inizio e di fine dell'effetto vengono ritagliate entro i limiti dell'intervallo di tempo dell'oggetto. Se è già presente un effetto al livello di priorità specificato, tutti gli effetti dal punto in poi spostano verso il basso l'elenco delle priorità per fare spazio al nuovo effetto.

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

[**Interfaccia IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




