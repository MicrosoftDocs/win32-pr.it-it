---
description: Il metodo GetEffect recupera l'effetto al livello di priorità specificato.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Metodo IAMTimelineEffectable:: GetEffect (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333694"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>Metodo IAMTimelineEffectable:: GetEffect

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **GetEffect** recupera l'effetto al livello di priorità specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFX* \[ out\]
</dt> <dd>

Riceve l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'effetto.

</dd> <dt>

*Che* 
</dt> <dd>

Livello di priorità dell'effetto da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HRESULT. I possibili valori sono i seguenti:



| Codice restituito                                                                               | Descrizione                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Nessun effetto alla priorità specificata,<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                             |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/>           |



 

## <a name="remarks"></a>Commenti

Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




