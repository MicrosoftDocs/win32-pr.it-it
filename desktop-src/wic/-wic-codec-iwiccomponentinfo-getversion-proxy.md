---
description: Funzione proxy per il metodo GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5a781aacbe0b5b9dd35a94c2ce906ee546e0b1da6b426a6848b6aafed2721cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965220"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>Funzione proxy IWICComponentInfo \_ GetVersion \_

Funzione proxy per il [**metodo GetVersion.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
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

*cchVersion* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni del buffer *wzVersion.*

</dd> <dt>

*wzVersion* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Puntatore che riceve una stringa invariante delle impostazioni cultura della versione del componente.

</dd> <dt>

*pcchActual* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve la lunghezza effettiva della versione del componente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




