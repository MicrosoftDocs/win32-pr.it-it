---
description: Funzione proxy per il metodo GetColorCount.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 18d06760c696bb3e95dc638bea31d02228a108b9866e213013243ad4eeec441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206330"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a>Funzione proxy IWICPalette \_ \_ GetColorCount

Funzione proxy per il [**metodo GetColorCount.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntatore a [**questo oggetto IWICPalette.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pcCount* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve il numero di colori nella tabella dei colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




