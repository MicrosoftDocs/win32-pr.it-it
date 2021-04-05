---
description: Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Funzione WldpIsDynamicCodePolicyEnabled (Wldp. h)
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
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125853"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>WldpIsDynamicCodePolicyEnabled (funzione)

Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsEnabled* \[ out\]
</dt> <dd>

In caso di esito positivo, restituisce **true** se i criteri di Device Guard applicano criteri di codice dinamici .NET; in caso contrario, restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="remarks"></a>Commenti

Il codice dinamico si riferisce al codice generato in modo dinamico CRL .NET.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




