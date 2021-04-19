---
description: Le costanti seguenti vengono utilizzate da PStore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Costanti PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328183"
---
# <a name="pstore-constants"></a>Costanti PStore

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Le costanti seguenti vengono utilizzate da PStore.

Codici di errore di archiviazione protetta



| Costante/valore                                                                                                                                                                                                                               | Descrizione                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**Pst \_ E \_ OK**</dt> <dt>0x00000000L</dt> </dl>                             | L'operazione è stata completata.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**Pst \_ \_Tipo E \_ esistente**</dt> <dt>0x800C0004L</dt> </dl> | L'elemento dati esiste già nell'archivio protetto. <br/> |



Valori della clausola di accesso



| Costante/valore                                                                                                                                                                                                                                      | Descrizione                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**Pst \_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Punta a una struttura di [**\_ AUTHENTICODEDATA PST**](pst-authenticodedata.md) .<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **\_ \_ Controllo binario PST**</dt> <dt>2</dt> </dl>                   | Punta a una struttura di **\_ BINARYCHECKDATA PST** .<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**Pst \_ \_Descrittore di sicurezza**</dt> <dt>4</dt> </dl> | Punta a un descrittore di sicurezza di Windows valido. <br/>                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



 

 
