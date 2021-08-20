---
description: Cancella le informazioni utente memorizzate nella cache dell'oggetto.
title: Metodo DIDiskQuotaUser.Invalidate
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
ms.openlocfilehash: c0c7235031b20749a1aecd647c49a66fb3af1d108f7b09aaf7f02166dba9428e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050731"
---
# <a name="didiskquotauserinvalidate-method"></a>Metodo DIDiskQuotaUser.Invalidate

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

Questo metodo cancella le informazioni utente archiviate nella cache dell'oggetto. Alla successiva richiesta di informazioni relative alla quota, l'oggetto recupera le informazioni dal volume NTFS e aggiorna la cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




