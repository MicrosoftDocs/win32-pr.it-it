---
description: Funzione proxy per il metodo GetColors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fca361a2e7385b4e3fb0757e28d25472ac84bc3fd4bb8d028406c51514ef9da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033547"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>Funzione proxy IWICPalette \_ \_ GetColors

Funzione proxy per il [**metodo GetColors.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntatore a [**questo oggetto IWICPalette.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*colorCount* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensione della matrice *pColors.*

</dd> <dt>

*pColors* \[ Cambio\]
</dt> <dd>

Tipo: **WICColor \***

Puntatore che riceve i colori della tavolozza.

</dd> <dt>

*pcActualColors* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Dimensioni effettive necessarie per ottenere i colori della tavolozza.

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



 

 




