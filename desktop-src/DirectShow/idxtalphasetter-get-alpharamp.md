---
description: Il \_ metodo Get AlphaRamp recupera la proprietà Alpha ramp. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Metodo IDxtAlphaSetter:: get_AlphaRamp (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326782"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>Metodo IDxtAlphaSetter:: Get \_ AlphaRamp

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_AlphaRamp` metodo recupera la proprietà della rampa alfa. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Riceve la rampa Alpha. Un valore negativo indica che non è impostata alcuna rampa alfa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                               | Descrizione                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null**<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                   |



 

## <a name="remarks"></a>Commenti

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
</dt> </dl>

 

 




