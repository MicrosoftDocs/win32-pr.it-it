---
description: Ottiene le proprietà della visualizzazione.
title: Metodo IShellFolderViewType::GetViewTypeProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: 57e053321bbd17c90fbe82832cdb01e9acb6994438d22cb72ef62bf1e7143dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220309"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Metodo IShellFolderViewType::GetViewTypeProperties

Ottiene le proprietà della visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Pollici\]
</dt> <dd>

Tipo: **PCUITEMID \_ CHILD**

Oggetto PIDL.

</dd> <dt>

*pdwFlags* \[ Cambio\]
</dt> <dd>

Tipo: **DWORD \***

Puntatore a una variabile unsigned integer che riceve le proprietà della visualizzazione, che indicano l'operazione da eseguire quando viene selezionata la vista. I flag possono essere qualsiasi combinazione dei valori seguenti.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)


</dt> <dd>

Se non è presente, creare un elemento di visualizzazione.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)


</dt> <dd>

Reinserisci PIDL e riordinamento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




