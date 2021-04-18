---
description: Funzione proxy per il metodo GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Funzione IWICComponentInfo_GetFriendlyName_Proxy
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
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314889"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>IWICComponentInfo \_ funzione proxy GetFriendlyName \_

Funzione proxy per il metodo [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .

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

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Puntatore a questo oggetto [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchFriendlyName* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni del buffer *wzFriendlyName* .

</dd> <dt>

*wzFriendlyName* \[ in uscita\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntatore che riceve il nome descrittivo del componente.

La stringa restituita è specifica delle impostazioni locali, 1033 per impostazione predefinita.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntatore che riceve la lunghezza effettiva del nome descrittivo del componente.

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



 

 




