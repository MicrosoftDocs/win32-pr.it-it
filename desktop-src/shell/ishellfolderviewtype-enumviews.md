---
description: Recupera un enumeratore che restituirà un puntatore a un elenco di identificatori di elemento (PIDL) per ogni visualizzazione estesa.
title: 'Metodo IShellFolderViewType:: EnumViews'
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
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993824"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>Metodo IShellFolderViewType:: EnumViews

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

*grfFlags* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Flag che indicano gli elementi da includere nell'enumerazione. Per un elenco di valori possibili, vedere il tipo enumerato [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) . Questo parametro può essere ignorato.

</dd> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Indirizzo di una variabile puntatore di tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) che riceve l'enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le visualizzazioni sono rappresentate all'utente come cartelle nascoste dalla directory radice (rappresentata da PIDL). Quando appropriato, la visualizzazione predefinita (disattivata nella cartella radice) viene rappresentata come **valore null** o vuoto, PIDL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




