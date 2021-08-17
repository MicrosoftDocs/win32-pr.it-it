---
description: Il metodo put \_ AlphaRamp specifica la proprietà alpha ramp. La rampa alfa è la percentuale in base alla quale vengono regolati i valori alfa nell'immagine originale. Ad esempio, se la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti del 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: Metodo IDxtAlphaSetter::p ut_AlphaRamp (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88661c40ea0824d643909f688a7d86251c434e0e3dcc88d8a3aec97dcb6b40c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952730"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>Metodo IDxtAlphaSetter::p ut \_ AlphaRamp

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `put_AlphaRamp` metodo specifica la proprietà alpha ramp. La rampa alfa è la percentuale in base alla quale vengono regolati i valori alfa nell'immagine originale. Ad esempio, se la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti del 50%.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Alfa* \[ Pollici\]
</dt> <dd>

Rampa alfa come percentuale. Ad esempio, 1,0 è 100%. Per disabilitare questa proprietà, impostare un valore negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se si imposta questa proprietà su un valore non negativo, è necessario disabilitare anche la proprietà alpha chiamando **put \_ Alpha** con un valore negativo. In caso contrario, il rendering dell'effetto non verrà eseguito correttamente.

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

[**Interfaccia IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::put \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




