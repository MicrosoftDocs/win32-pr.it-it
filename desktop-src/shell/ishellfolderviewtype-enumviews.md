---
description: Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.
title: Metodo IShellFolderViewType::EnumViews
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842772"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>Metodo IShellFolderViewType::EnumViews

Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*grfFlags* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Flag che indicano gli elementi da includere nell'enumerazione . Per un elenco dei valori possibili, vedere il [**tipo enumerato SHCONTF.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) Questo parametro può essere ignorato.

</dd> <dt>

*ppenum* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Indirizzo di una variabile puntatore di tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) che riceve l'enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le visualizzazioni vengono rappresentate all'utente come cartelle nascoste dalla directory radice (rappresentate da PIDL). Se appropriato, la visualizzazione predefinita (all'di fuori della cartella radice) viene rappresentata come **NULL** o come PIDL vuoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




