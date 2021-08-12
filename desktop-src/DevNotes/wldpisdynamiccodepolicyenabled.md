---
description: Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Funzione WldpIsDynamicCodePolicyEnabled (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 12643bd542acac908c560a2094fb02e69d6d1aae62308e4ca4ece3be8bb85c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666362"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>Funzione WldpIsDynamicCodePolicyEnabled

Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isEnabled* \[ Cambio\]
</dt> <dd>

In caso di esito **positivo, restituisce true** se i criteri di Device Guard applicano i criteri del codice dinamico .NET. In caso contrario, **restituisce false.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S \_ OK in caso** di esito positivo o un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Il codice dinamico fa riferimento al codice CRL .NET generato dinamicamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1803 \[\]<br/>                           |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




