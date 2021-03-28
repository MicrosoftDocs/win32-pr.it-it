---
description: Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella della shell in una rappresentazione diversa.
title: 'Metodo IShellFolderViewType:: TranslateViewPidl'
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
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527312"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>Metodo IShellFolderViewType:: TranslateViewPidl

Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella della shell in una rappresentazione diversa.

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

*PIDL* \[ in\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

Matrice di ID elemento rispetto alla cartella radice.

</dd> <dt>

*pidlView* \[ in\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

PIDL speciale della visualizzazione.

</dd> <dt>

*ppidlOut* \[ in\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo \** _

Indirizzo di una variabile PIDL per ricevere la traduzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Al termine, è necessario liberare il PIDL restituito con [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




