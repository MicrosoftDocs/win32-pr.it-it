---
description: Recupera il valore di un'opzione di Microsoft .NET di accesso Passport specifica.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: Metodo IPassportManager3::get_Option
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5d7260e3c13be21f1cc963e1bca15a6126739a0075b94ee11f07d98901efd39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750041"
---
# <a name="ipassportmanager3get_option-method"></a>Metodo IPassportManager3::get \_ Option

Recupera il valore di un'opzione di Microsoft .NET di accesso Passport specifica.

> [!Note]  
> Il **metodo \_ get Option** appartiene all'interfaccia [**IPassportManager3.**](/previous-versions/ms817681(v=msdn.10)) Questo argomento integra la documentazione iniziale.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

Opzione di accesso da recuperare. Attualmente, l'unica opzione supportata è "iMode".

</dd> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore a **UN VARIANT** (VT \_ BOOL) che riceve il valore dell'opzione. Questo valore può essere True o False.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK quando il metodo ha esito positivo.

## <a name="remarks"></a>Commenti

Questo metodo viene fornito con le versioni precedenti di Passport SDK.

 

 
