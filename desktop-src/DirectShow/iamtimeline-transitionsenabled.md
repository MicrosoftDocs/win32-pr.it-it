---
description: Il metodo TransitionsEnabled determina se le transizioni sono abilitate.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Metodo IAMTimeline:: TransitionsEnabled (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330189"
---
# <a name="iamtimelinetransitionsenabled-method"></a>Metodo IAMTimeline:: TransitionsEnabled

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **TransitionsEnabled** determina se le transizioni sono abilitate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Riceve un valore booleano. Se **true**, le transizioni sono abilitate. In caso contrario, le transizioni sono disabilitate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




