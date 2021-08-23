---
description: Funzione proxy per il metodo GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5af41c00945550fc9e833b9324e22f522aa7a5e73dacd109d76159d5dd0173db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965250"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>Funzione proxy IWICComponentInfo \_ GetFriendlyName \_

Funzione proxy per il [**metodo GetFriendlyName.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
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

*cchFriendlyName* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni del buffer *wzFriendlyName.*

</dd> <dt>

*wzFriendlyName* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Puntatore che riceve il nome descrittivo del componente.

La stringa restituita è specifica delle impostazioni locali, 1033 per impostazione predefinita.

</dd> <dt>

*pcchActual* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve la lunghezza effettiva del nome descrittivo del componente.

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



 

 




