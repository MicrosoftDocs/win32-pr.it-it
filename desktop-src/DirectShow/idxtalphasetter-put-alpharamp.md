---
description: Il \_ metodo Put AlphaRamp specifica la proprietà della rampa Alpha. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: metodo:p ut_AlphaRamp (qedit. h)'
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
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333432"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter::p UT \_ AlphaRamp metodo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_AlphaRamp` metodo specifica la proprietà della rampa alfa. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Alfa* \[ in\]
</dt> <dd>

La rampa alfa come percentuale. Ad esempio, 1,0 è 100%. Per disabilitare questa proprietà, impostare un valore negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se si imposta questa proprietà su un valore non negativo, è necessario disabilitare anche la proprietà Alpha, chiamando **put \_ Alpha** con un valore negativo. In caso contrario, non viene eseguito il rendering corretto dell'effetto.

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

[**Interfaccia IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::p UT \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




