---
description: Cancella il nome utente dal controllo smart card.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Metodo ISCrdEnr:: resetUser'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317714"
---
# <a name="iscrdenrresetuser-method"></a>Metodo ISCrdEnr:: resetUser

Il metodo **resetUser** Cancella il nome utente dal controllo smart card.

## <a name="syntax"></a>Sintassi


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Questo metodo cancella qualsiasi nome utente esistente e certificato registrato in precedenza dalla memoria. Tuttavia, il certificato registrato in precedenza non viene rimosso dalla smart card.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr:: seusername**](iscrdenr-setusername.md)
</dt> </dl>

 

 




