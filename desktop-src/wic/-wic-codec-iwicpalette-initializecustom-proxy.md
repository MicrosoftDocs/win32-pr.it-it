---
description: Funzione proxy per il metodo InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b68917782d768f526a21b16f22766c1a9add61eb5ee1987d27965b6f70a388db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088193"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a>Funzione IWICPalette \_ InitializeCustom \_ Proxy

Funzione proxy per il [**metodo InitializeCustom.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntatore a [**questo oggetto IWICPalette.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pColors* \[ Pollici\]
</dt> <dd>

Tipo: **WICColor \***

Puntatore alla matrice di colori.

</dd> <dt>

*colorCount* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero di colori in *pColors.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop di Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




