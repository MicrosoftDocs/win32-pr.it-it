---
description: Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel registro di sistema.
title: REGSAM (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983086"
---
# <a name="regsam"></a>REGSAM

Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel registro di sistema.



| Costante                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**CHIAVE \_ tutti gli \_ accessi**</dt> </dl>                          | Combinazione di * * * * \_ valore query chiave \_ * * * *, * * * * chiave \_ enumerazione \_ \_ sottochiavi * * * *, * * * * notifica chiave * * * * \_ , * * * * chiave \_ creazione della chiave \_ secondaria * * * * \_ , * * * * chiave \_ creazione \_ collegamento * * * * e * \_ \_ * * * * * * * * * * * * * *<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_collegamento creazione \_ chiave**</dt> </dl>                       | Autorizzazione per creare un collegamento simbolico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**CHIAVE \_ creazione chiave \_ secondaria \_**</dt> </dl>             | Autorizzazione per la creazione di sottochiavi.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**CHIAVE \_ enumerazione \_ \_ sottochiavi**</dt> </dl> | Autorizzazione per enumerare le sottochiavi.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**esecuzione della chiave \_**</dt> </dl>                                    | Autorizzazione per l'accesso in lettura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**\_notifica chiave**</dt> </dl>                                       | Autorizzazione per la notifica di modifica.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**\_valore query \_ chiave**</dt> </dl>                       | Autorizzazione per eseguire query sui dati della sottochiave.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**\_lettura chiave**</dt> </dl>                                             | Combinazione di * * * * \_ valore di query chiave \_ * * * *, * * * * \_ enumerazione \_ chiavi \_ sottochiavi * * * * e * * * * * * * * \_ notifica chiave * * * * accesso.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**\_valore del set di chiavi \_**</dt> </dl>                             | Autorizzazione per impostare i dati della sottochiave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**\_scrittura chiave**</dt> </dl>                                          | Combinazione di * * * * valore del set di chiavi \_ \_ * * * * e * * * * chiave \_ creazione della \_ \_ sottochiave * * * * accesso.<br/>                                                                                                                |



## <a name="remarks"></a>Commenti

Un valore **REGSAM** può essere costituito da uno o più valori elencati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




