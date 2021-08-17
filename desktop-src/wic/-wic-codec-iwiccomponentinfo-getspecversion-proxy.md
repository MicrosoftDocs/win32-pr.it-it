---
description: Funzione proxy per il metodo GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a29b57e84b7cf9ceee67ac4f64ac090e697366fbe0698a891c8fbcc87e3ff5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206584"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>Funzione proxy IWICComponentInfo \_ GetSpecVersion \_

Funzione proxy per il [**metodo GetSpecVersion.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Puntatore a [**questo oggetto IWICComponentInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchSpecVersion* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni del buffer *wzSpecVersion.*

</dd> <dt>

*wzSpecVersion* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Quando questo metodo viene restituito, contiene una stringa invariabile delle impostazioni cultura della versione della specifica del componente. Il formato della versione è NN.NN.NN.NN.

</dd> <dt>

*pcchActual* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve la lunghezza effettiva della versione della specifica del componente.

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



 

 




