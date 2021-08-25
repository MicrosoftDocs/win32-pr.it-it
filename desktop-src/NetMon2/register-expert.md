---
description: L'esperto deve implementare la funzione Register Expert. Network Monitor chiama la funzione Register Expert per ottenere informazioni sull'esperto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrare la funzione di callback Expert (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 1203682e82b01b7665c9661c3f58c14bbf2cd479cac62c72a64505b0e25feaa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889571"
---
# <a name="register-expert-callback-function"></a>Funzione di callback Register Expert

L'esperto deve **implementare la funzione Register** Expert. Network Monitor chiama la **funzione Register** Expert per ottenere informazioni sull'esperto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pExpertInfo* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura EXPERTENUMINFO**](expertenuminfo.md) Network Monitor allocata. L'esperto compila la struttura con tutte le informazioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **TRUE** e la funzione restituisce le informazioni richieste.

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Il **membro Version** della struttura [**EXPERTENUMINFO**](expertenuminfo.md) deve essere zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




