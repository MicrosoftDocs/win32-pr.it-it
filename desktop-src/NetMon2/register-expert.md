---
description: L'esperto deve implementare la funzione Register Expert. Network Monitor chiama la funzione Register Expert per ottenere informazioni sull'esperto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Funzione Register Expert callback (Netmon. h)
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
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880706"
---
# <a name="register-expert-callback-function"></a>Registra funzione di callback esperto

L'esperto deve implementare la funzione **Register** Expert. Network Monitor chiama la funzione **Register** Expert per ottenere informazioni sull'esperto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pExpertInfo* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**EXPERTENUMINFO**](expertenuminfo.md) che Network Monitor alloca. L'esperto compila la struttura con tutte le informazioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **true** e la funzione restituisce le informazioni richieste.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Il membro della **versione** della struttura [**EXPERTENUMINFO**](expertenuminfo.md) deve essere zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




