---
description: Il metodo SetCutsOnly specifica se il rendering della transizione viene eseguito come taglio. In tal caso, la transizione si verifica immediatamente in corrispondenza del punto di taglio. Se il rendering di una transizione richiede molto tempo, è consigliabile visualizzarne l'anteprima come anteprima tagliata a velocità.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: Metodo IAMTimelineTrans::SetCutsOnly (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154728"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Metodo IAMTimelineTrans::SetCutsOnly

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetCutsOnly` metodo specifica se il rendering della transizione viene eseguito come taglio. In tal caso, la transizione si verifica immediatamente in corrispondenza del punto di taglio. Se il rendering di una transizione richiede molto tempo, è consigliabile visualizzarne l'anteprima come anteprima tagliata a velocità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* 
</dt> <dd>

Specifica se eseguire il rendering della transizione come taglio. Se **TRUE,** il rendering della transizione viene eseguito come taglio istantaneo. Se **FALSE,** il rendering della transizione viene eseguito sulla durata normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il rendering di una transizione come taglio non è compatibile con lo scambio degli input. Vedere [**IAMTimelineTrans::SetSwapInputs.**](iamtimelinetrans-setswapinputs.md) Se si chiama `SetCutsOnly` con un valore **TRUE**, viene temporaneamente eseguito l'override **dell'impostazione SetSwapInputs.** L'impostazione di sola riduzione è destinata all'anteprima, pertanto questa limitazione non influisce sull'output del file, ma ricordarsi di chiamare con il valore FALSE prima di `SetCutsOnly` scrivere il file. 

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




