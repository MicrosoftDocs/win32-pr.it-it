---
description: Verifica che il profilo utente online sia caricato.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Funzione OnProfileLoaded (Lsaidprov. h)
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
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756434"
---
# <a name="onprofileloaded-function"></a>OnProfileLoaded (funzione)

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

*ProviderHandle* \[ in\]
</dt> <dd>

Handle del provider.

</dd> <dt>

*UserToken* \[ in\]
</dt> <dd>

Token dell'utente di cui è in corso il caricamento o lo scaricamento del profilo.

</dd> <dt>

Con *caricamento* \[ in\]
</dt> <dd>

**True** se il profilo è stato caricato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.

Se la funzione ha esito negativo, la funzione restituisce un codice di errore diverso da zero che è un errore specifico del provider a scopo diagnostico.

## <a name="remarks"></a>Commenti

Questa funzione viene chiamata ogni volta che viene chiamata la funzione [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) . Non è sincronizzato con **LoadUserProfile**; ovvero è possibile che sia stato restituito **LoadUserProfile** e che il profilo sia stato scaricato dal momento in cui è stata chiamata la funzione. Questa funzione può essere chiamata più volte anche quando il profilo è stato caricato. Il provider di identità non deve presupporre che una chiamata a questa funzione con *Loaded* uguale a true sarà seguita da una chiamata con *Loaded* uguale a false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

 
