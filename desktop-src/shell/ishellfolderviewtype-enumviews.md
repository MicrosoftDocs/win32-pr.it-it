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
ms.openlocfilehash: 203ee36994ca3a622d564f637598f4ef22b8494200e5d57faa1d47cb290fd49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220337"
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

Flag che indicano quali elementi includere nell'enumerazione. Per un elenco dei valori possibili, vedere il [**tipo enumerato SHCONTF.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) Questo parametro può essere ignorato.

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

Le visualizzazioni sono rappresentate dall'utente come cartelle nascoste dalla directory radice (rappresentate da PID). Quando appropriato, la visualizzazione predefinita (all'di fuori della cartella radice) viene rappresentata come **NULL** o come PIDL vuoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




