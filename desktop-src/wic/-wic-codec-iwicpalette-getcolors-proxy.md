---
description: Funzione proxy per il metodo getcolors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Funzione IWICPalette_GetColors_Proxy
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
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232475"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>\_Funzione proxy IWICPalette Getcolors \_

Funzione proxy per il metodo [**Getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .

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

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Puntatore a questo oggetto [_ *IWICPalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .

</dd> <dt>

*colorCount* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni della matrice *pColors* .

</dd> <dt>

*pColors* \[ out\]
</dt> <dd>

Tipo: **WICColor \** _

Puntatore che riceve i colori della tavolozza.

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Dimensioni effettive necessarie per ottenere i colori della tavolozza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




