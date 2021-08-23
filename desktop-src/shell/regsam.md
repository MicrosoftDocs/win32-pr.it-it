---
description: Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel Registro di sistema.
title: REGSAM (Winnt.h)
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
ms.openlocfilehash: e202e615561ce0c51f44fc39726d8ab864afc2b5e1bcbbe5612edbb74c476c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820421"
---
# <a name="regsam"></a>REGSAM

Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel Registro di sistema.



| Costante                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**CHIAVE \_ ALL \_ ACCESS**</dt> </dl>                          | Combinazione di ****KEY \_ QUERY \_ VALUE***, ****KEY \_ ENUMERATE SUB \_ \_ KEYS***, ****KEY \_ NOTIFY***, ***KEY \_ CREATE SUB \_ \_ KEY***, ***KEY \_ CREATE \_ LINK**** e ***KEY \_ SET \_ VALUE****.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**COLLEGAMENTO DI \_ CREAZIONE \_ CHIAVE**</dt> </dl>                       | Autorizzazione per creare un collegamento simbolico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**CHIAVE \_ CREATE \_ SUB \_ KEY**</dt> </dl>             | Autorizzazione per la creazione di sottochiavi.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**CHIAVI \_ ENUMERATE \_ SUB \_ KEYS**</dt> </dl> | Autorizzazione per enumerare le sottochiavi.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**KEY \_ EXECUTE**</dt> </dl>                                    | Autorizzazione per l'accesso in lettura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**NOTIFICA \_ DELLA CHIAVE**</dt> </dl>                                       | Autorizzazione per la notifica delle modifiche.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**VALORE \_ DI QUERY \_ CHIAVE**</dt> </dl>                       | Autorizzazione per eseguire query sui dati delle sottochiavi.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**LETTURA \_ DELLA CHIAVE**</dt> </dl>                                             | Combinazione dell'accesso ****KEY \_ QUERY \_ VALUE***, ***KEY \_ ENUMERATE SUB \_ \_ KEYS*** e ***KEY \_ NOTIFY****.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**VALORE \_ DEL SET DI \_ CHIAVI**</dt> </dl>                             | Autorizzazione per impostare i dati delle sottochiavi.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**KEY \_ WRITE**</dt> </dl>                                          | Combinazione di accesso ****KEY \_ SET \_ VALUE**** e ***KEY \_ CREATE SUB \_ \_ KEY****.<br/>                                                                                                                |



## <a name="remarks"></a>Commenti

Un **valore REGSAM** può essere uno o più dei valori elencati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 




