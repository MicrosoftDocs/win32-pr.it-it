---
description: Verifica che il profilo utente online sia caricato.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Funzione OnProfileLoaded (Lsaidprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 6a8ed0d96ab7c9c63f9574472cac0daedba54e42beec244271efcc309c04dd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921145"
---
# <a name="onprofileloaded-function"></a>Funzione OnProfileLoaded

Verifica che il profilo utente online sia caricato.

## <a name="syntax"></a>Sintassi


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProviderHandle* \[ Pollici\]
</dt> <dd>

Handle del provider.

</dd> <dt>

*UserToken* \[ Pollici\]
</dt> <dd>

Token dell'utente il cui profilo viene caricato o scaricato.

</dd> <dt>

*Caricato* \[ Pollici\]
</dt> <dd>

**TRUE** se il profilo è stato caricato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce STATUS \_ SUCCESS.

Se la funzione ha esito negativo, la funzione restituisce un codice di errore diverso da zero che è un errore specifico del provider a scopo diagnostico.

## <a name="remarks"></a>Commenti

Questa funzione viene chiamata ogni volta che viene chiamata la funzione [**LoadUserProfile.**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) Non è sincronizzato con **LoadUserProfile.** è possibile che **LoadUserProfile abbia** restituito e che il profilo sia stato scaricato al momento della chiamata della funzione. Questa funzione può essere chiamata più volte anche quando il profilo è stato caricato. Il provider di identità non deve presupporre che una chiamata a questa funzione con *Loaded* uguale a TRUE sia seguita da una chiamata con *Loaded* uguale a FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Lsaidprov.h</dt> </dl> |



 

 
