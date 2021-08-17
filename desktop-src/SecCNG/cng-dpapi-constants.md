---
description: Le costanti seguenti vengono usate dal Data Protection API CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Costanti DPAPI CNG (NCryptprotect.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afc589afa113250728b46639b7cd47442034f7b3bc82264099f334919a94c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908799"
---
# <a name="cng-dpapi-constants"></a>Costanti DPAPI CNG

Le costanti seguenti vengono usate dal Data Protection API CNG.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**DELIMITATORE DESCR NCRYPT \_ \_ \_ E**
</dt> <dd> <dl> <dt>

L" E "
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un delimitatore AND.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ DESCR \_ UGUALE**
</dt> <dd> <dl> <dt>

L"="
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un segno di uguale.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**DELIMITATORE DESCR NCRYPT \_ \_ \_ O**
</dt> <dd> <dl> <dt>

L" OR "
</dt> <dt>



Può essere usato per testare una stringa del descrittore di protezione per un delimitatore OR.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**ALGORITMO DI PROTEZIONE DELLE CHIAVI NCRYPT \_ \_ \_ \_ LOCALE**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



Il descrittore di protezione LOCAL protegge il contenuto per la sessione di accesso, l'utente corrente o il computer locale, come identificato dalle costanti seguenti:

-   **ACCESSO LOCALE DI NCRYPT \_ KEY \_ \_ \_ PROTECTION**
-   **UTENTE LOCALE DI PROTEZIONE \_ \_ DELLE CHIAVI \_ NCRYPT \_**
-   **COMPUTER LOCALE \_ DI PROTEZIONE \_ DELLE CHIAVI \_ NCRYPT \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**SDDL DELL'ALGORITMO DI PROTEZIONE \_ \_ DELLE \_ \_ CHIAVI NCRYPT**
</dt> <dd> <dl> <dt>

"SDDL"
</dt> <dt>



Protegge il contenuto in una stringa SDDL (Security Descriptor Definition Language) che contiene informazioni sul descrittore di sicurezza.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**SID DELL'ALGORITMO NCRYPT \_ KEY \_ \_ PROTECTION \_**
</dt> <dd> <dl> <dt>

"SID"
</dt> <dt>



Il descrittore di protezione SID contiene un'identità di gruppo o entità.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_WEBCREDENTIALS \_ \_ DELL'ALGORITMO DI \_ PROTEZIONE DELLE CHIAVI NCRYPT**
</dt> <dd> <dl> <dt>

"WEBCREDENTIALS"
</dt> <dt>



Protegge dalle credenziali dell'account Web di un utente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**ACCESSO LOCALE DI NCRYPT \_ KEY \_ \_ \_ PROTECTION**
</dt> <dd> <dl> <dt>

"logon"
</dt> <dt>



Protegge il contenuto della sessione di accesso corrente. Gli utenti non potranno decrittografare il contenuto protetto dopo la disconnessione o il riavvio.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**COMPUTER LOCALE \_ DI PROTEZIONE \_ DELLE CHIAVI \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

"computer"
</dt> <dt>



Protegge il contenuto nel computer locale. Tutti gli utenti nel computer locale possono decrittografare il contenuto protetto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**UTENTE LOCALE DI PROTEZIONE \_ \_ DELLE CHIAVI \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

"user"
</dt> <dt>



Protegge il contenuto della sessione utente corrente. Solo questo utente nel computer locale sarà in grado di decrittografare il contenuto protetto.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**PROVIDER \_ DI PROTEZIONE DELLA CHIAVE \_ \_ MS**
</dt> <dd> <dl> <dt>

"Provider di protezione delle chiavi Microsoft"
</dt> <dt>



Rappresenta il provider di protezione delle chiavi Microsoft che supporta i formati rappresentati dalle costanti seguenti:

-   **SID DELL'ALGORITMO NCRYPT \_ KEY \_ \_ PROTECTION \_**
-   **ALGORITMO DI PROTEZIONE DELLE CHIAVI NCRYPT \_ \_ \_ \_ LOCALE**
-   **SDDL DELL'ALGORITMO DI PROTEZIONE \_ \_ DELLE \_ \_ CHIAVI NCRYPT**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_PROVIDER DI PROTEZIONE DELLE CHIAVI CLIENT \_ \_ \_ WINDOWS**
</dt> <dd> <dl> <dt>

"Windows provider di protezione delle chiavi client"
</dt> <dt>



Rappresenta il provider di protezione delle chiavi Microsoft disponibile solo nel client e che supporta i formati rappresentati dalle costanti seguenti:

-   **\_WEBCREDENTIALS \_ \_ DELL'ALGORITMO DI \_ PROTEZIONE DELLE CHIAVI NCRYPT**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NCryptprotect.h</dt> </dl> |



 

 




