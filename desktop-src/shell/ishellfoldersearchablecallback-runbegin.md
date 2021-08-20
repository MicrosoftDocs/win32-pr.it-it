---
description: Indica che è stata avviata una ricerca.
title: Metodo IShellFolderSearchableCallback::RunBegin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 026b5b458736a0805d48dc59715a1705ecdb8557037232332767946dd05d333d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223351"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a>Metodo IShellFolderSearchableCallback::RunBegin

Indica che è stata avviata una ricerca.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwReserved* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

In risposta a questo callback, l'applicazione può ad esempio abilitare **il pulsante** Annulla.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




