---
description: Le costanti seguenti vengono utilizzate dall'Data Protection API CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Costanti DPAPI CNG (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484292"
---
# <a name="cng-dpapi-constants"></a>Costanti DPAPI CNG

Le costanti seguenti vengono utilizzate dall'Data Protection API CNG.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_DElimitatore NCRYPT descr \_ \_ e**
</dt> <dd> <dl> <dt>

L "E"
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un delimitatore e.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ Descr \_ uguale a**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un segno di uguale.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_DElimitatore NCRYPT descr \_ \_ o**
</dt> <dd> <dl> <dt>

L "O"
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un delimitatore o.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algoritmo di protezione con chiave NCRYPT \_ \_ \_ locale**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



Il descrittore di protezione locale protegge il contenuto della sessione di accesso, dell'utente corrente o del computer locale come identificato dalle costanti seguenti:

-   **\_ \_ \_ accesso locale per la protezione della chiave NCRYPT \_**
-   **utente locale di NCRYPT \_ Key \_ Protection \_ \_**
-   **\_ \_ computer locale di protezione con chiave NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_ \_ SDDL algoritmo di protezione con chiave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



Protegge il contenuto in una stringa SDDL (Security Descriptor Definition Language) che contiene informazioni sul descrittore di sicurezza.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_ \_ SID algoritmo di protezione con chiave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

SID
</dt> <dt>



Il descrittore di protezione SID contiene un'identità di gruppo o entità.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_ \_ \_ credenziali webcredentials dell'algoritmo NCRYPT Key Protection \_**
</dt> <dd> <dl> <dt>

"Webcredentials"
</dt> <dt>



Protegge le credenziali dell'account Web di un utente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_ \_ \_ accesso locale per la protezione della chiave NCRYPT \_**
</dt> <dd> <dl> <dt>

accesso
</dt> <dt>



Protegge il contenuto nella sessione di accesso corrente. Gli utenti non saranno in grado di decrittografare il contenuto protetto dopo la disconnessione o il riavvio.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ computer locale di protezione con chiave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

macchina
</dt> <dt>



Protegge il contenuto nel computer locale. Tutti gli utenti del computer locale possono decrittografare il contenuto protetto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**utente locale di NCRYPT \_ Key \_ Protection \_ \_**
</dt> <dd> <dl> <dt>

utente
</dt> <dt>



Protegge il contenuto nella sessione utente corrente. Solo questo utente nel computer locale sarà in grado di decrittografare il contenuto protetto.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_provider di \_ protezione con chiave MS \_**
</dt> <dd> <dl> <dt>

"Provider Microsoft per la protezione delle chiavi"
</dt> <dt>



Rappresenta il provider Microsoft per la protezione delle chiavi che supporta formati rappresentati dalle costanti seguenti:

-   **\_ \_ SID algoritmo di protezione con chiave NCRYPT \_ \_**
-   **\_algoritmo di protezione con chiave NCRYPT \_ \_ \_ locale**
-   **\_ \_ SDDL algoritmo di protezione con chiave NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_provider di \_ protezione con chiave client \_ Windows \_**
</dt> <dd> <dl> <dt>

"Windows client key protection provider"
</dt> <dt>



Rappresenta il provider di protezione con chiave Microsoft disponibile solo nel client e che supporta formati rappresentati dalle costanti seguenti:

-   **\_ \_ \_ credenziali webcredentials dell'algoritmo NCRYPT Key Protection \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NCryptprotect. h</dt> </dl> |



 

 




