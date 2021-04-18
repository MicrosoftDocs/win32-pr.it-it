---
description: Ottiene le proprietà della visualizzazione.
title: 'Metodo IShellFolderViewType:: GetViewTypeProperties'
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
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977927"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Metodo IShellFolderViewType:: GetViewTypeProperties

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

*PIDL* \[ in\]
</dt> <dd>

Tipo: **PCUITEMID \_ figlio**

PIDL.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Tipo: **DWORD \** _

Puntatore a una variabile Unsigned Integer che riceve le proprietà di visualizzazione, che indicano l'azione da eseguire quando la visualizzazione è selezionata. I flag possono essere costituiti da qualsiasi combinazione dei valori seguenti.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ Notify \_ create** (0x00000001)


</dt> <dd>

Crea elemento visualizzazione se non è presente.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ Resort** (0x00000002)


</dt> <dd>

Reinserire PIDL ed eseguire di nuovo l'ordinamento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




