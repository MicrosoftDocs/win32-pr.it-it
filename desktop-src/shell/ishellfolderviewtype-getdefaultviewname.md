---
description: Ottiene il nome della visualizzazione predefinita. Chiamare GetDisplayNameOf per recuperare i nomi delle altre visualizzazioni.
title: Metodo IShellFolderViewType::GetDefaultViewName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842762"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>Metodo IShellFolderViewType::GetDefaultViewName

Ottiene il nome della visualizzazione predefinita. Chiamare [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperare i nomi delle altre visualizzazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag uFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Flag facoltativi; deve essere impostato su 0.

</dd> <dt>

*ppwszName* \[ Cambio\]
</dt> <dd>

Tipo: **LPWSTR \***

Indirizzo di un puntatore di stringa che riceve il nome di visualizzazione predefinito. La memoria per la stringa viene allocata [**con SHStrDup.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




