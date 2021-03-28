---
description: Cancella le informazioni utente memorizzate nella cache dell'oggetto.
title: DIDiskQuotaUser. Invalidate (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525344"
---
# <a name="didiskquotauserinvalidate-method"></a>DIDiskQuotaUser. Invalidate (metodo)

Cancella le informazioni utente memorizzate nella cache dell'oggetto.

## <a name="syntax"></a>Sintassi


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo consente di cancellare le informazioni utente archiviate nella cache dell'oggetto. La volta successiva che viene effettuata una richiesta per le informazioni relative alla quota, l'oggetto recupera le informazioni dal volume NTFS e aggiorna la cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




