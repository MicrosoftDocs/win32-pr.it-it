---
description: Inizia una ricerca di una stringa di ricerca specificata.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Metodo IShellFolderSearchable:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753063"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Metodo IShellFolderSearchable:: FindString

Inizia una ricerca di una stringa di ricerca specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszTarget* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica la parola chiave search.

</dd> <dt>

*pdwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD \** _

Nessun flag attualmente definito. impostare su _ * NULL * *.

</dd> <dt>

*punkOnAsyncSearch* \[ in\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntatore a un oggetto di tipo [_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown). Questo oggetto deve supportare l'interfaccia [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) . Impostare su **null** se non è necessario alcun callback.

</dd> <dt>

*ppidlOut* \[ out\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Puntatore a una struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
