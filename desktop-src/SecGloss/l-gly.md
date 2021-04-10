---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera L.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883277"
---
# <a name="l-security-glossary"></a>L (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**LDAP**
</dt> <dd>

Vedere *Lightweight Directory Access Protocol*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Lightweight Directory Access Protocol**
</dt> <dd>

Un subset più semplice implementato dello standard X. 500 DAP per i servizi directory.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**Little-Endian**
</dt> <dd>

Memoria o formato di dati in cui il byte meno significativo viene archiviato nell'indirizzo inferiore o arriva per primo.

Vedere anche [*Big-Endian*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**Identificatore univoco locale**
</dt> <dd>

LUID Valore a 64 bit che garantisce l'univocità nel sistema operativo che lo ha generato fino al riavvio del sistema.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**autorità di registrazione locale**
</dt> <dd>

LRA Intermediario tra un server di pubblicazione e un' [*autorità di certificazione*](c-gly.md) (CA). L'LRA può, ad esempio, verificare le credenziali di un editore prima di inviarle alla CA.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Autorità di sicurezza locale**
</dt> <dd>

LSA Un sottosistema protetto che autentica e registra gli utenti nel sistema locale. LSA mantiene inoltre le informazioni su tutti gli aspetti della sicurezza locale in un sistema, noti collettivamente come criteri di sicurezza locali del sistema.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**Archivio logico**
</dt> <dd>

Vedere [*archivio virtuale*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**dati di accesso**
</dt> <dd>

Informazioni presentate al sistema da un' [*entità di sicurezza*](s-gly.md) per l'autenticazione.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**identificatore di accesso**
</dt> <dd>

Oggetto LUID che identifica una *sessione di accesso*. Un ID di accesso è valido fino a quando l'utente non si disconnette. Un ID di accesso è univoco durante l'esecuzione del computer; nessun'altra sessione di accesso avrà lo stesso ID di accesso. Tuttavia, il set di possibili ID di accesso viene reimpostato all'avvio del computer. Per recuperare l'ID di accesso da un [*token di accesso*](a-gly.md), chiamare la funzione **GetTokenInformation** per TokenStatistics; l'ID di accesso è nel membro **AuthenticationId** .

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**sessione di accesso**
</dt> <dd>

Una sessione di accesso viene avviata ogni volta che un utente accede a un computer. Tutti i processi in una sessione di accesso hanno lo stesso [*token di accesso*](a-gly.md)primario. Il token di accesso contiene informazioni sul contesto di sicurezza della sessione di accesso, inclusi il SID dell'utente, l' *identificatore di accesso* e il SID di *accesso*.

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**SID di accesso**
</dt> <dd>

[*ID di sicurezza*](s-gly.md) (SID) che identifica una *sessione di accesso*. È possibile utilizzare il SID di accesso in un [*DACL*](d-gly.md) per controllare l'accesso durante una sessione di accesso. Un SID di accesso è valido fino a quando l'utente non si disconnette. Un SID di accesso è univoco durante l'esecuzione del computer; nessun'altra sessione di accesso avrà lo stesso SID di accesso. Tuttavia, il set di possibili SID di accesso viene reimpostato all'avvio del computer. Per recuperare il SID di accesso da un [*token di accesso*](a-gly.md), chiamare la funzione **GetTokenInformation** per tokenGroups.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**funzioni di messaggio di basso livello**
</dt> <dd>

Funzioni di gestione dei messaggi che operano a un livello superiore rispetto alle funzioni di crittografia di base. Queste funzioni forniscono funzionalità per la codifica dei dati per la trasmissione e la decodifica dei dati ricevuti. Le funzioni di messaggio di basso livello offrono maggiore flessibilità rispetto alle funzioni di messaggio semplificate, ma richiedono più chiamate di funzione.

Vedere anche [*funzioni di messaggio semplificate*](s-gly.md).

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**LSA**
</dt> <dd>

Vedere *autorità di sicurezza locale*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

Vedere *identificatore univoco locale*.

</dd> </dl>

 

 



