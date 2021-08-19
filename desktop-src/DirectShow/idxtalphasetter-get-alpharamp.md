---
description: Il metodo get \_ AlphaRamp recupera la proprietà alpha ramp. La rampa alfa è la percentuale in base alla quale vengono regolati i valori alfa nell'immagine originale. Ad esempio, se la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti del 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: Metodo IDxtAlphaSetter::get_AlphaRamp (Qedit.h)
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
ms.openlocfilehash: 9768ed96f0b40e074fd44de04ca44a8cc17d9de7ce4b75af948975e26b5e3077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952740"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>Metodo IDxtAlphaSetter::get \_ AlphaRamp

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_AlphaRamp` metodo recupera la proprietà alpha ramp. La rampa alfa è la percentuale in base alla quale vengono regolati i valori alfa nell'immagine originale. Ad esempio, se la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti del 50%.

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

Riceve la rampa alfa. Un valore negativo indica che non è impostata alcuna rampa alfa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                               | Descrizione                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | **Argomento puntatore NULL**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                   |



 

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




