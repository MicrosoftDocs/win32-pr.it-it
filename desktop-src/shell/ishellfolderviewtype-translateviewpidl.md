---
description: Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella Shell in una rappresentazione diversa.
title: Metodo IShellFolderViewType::TranslateViewPidl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842672"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>Metodo IShellFolderViewType::TranslateViewPidl

Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella Shell in una rappresentazione diversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Pollici\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE**

Matrice di ID elemento relativi alla cartella radice.

</dd> <dt>

*pidlView* \[ Pollici\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE**

PIDL speciale della vista.

</dd> <dt>

*ppidlOut* \[ Pollici\]
</dt> <dd>

Tipo: **PCUIDLIST \_ RELATIVE \***

Indirizzo di una variabile PIDL per ricevere la traduzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Al termine, è necessario liberare il FILE PIDL restituito con [**ILFree.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




