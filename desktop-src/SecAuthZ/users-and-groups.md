---
description: Viene illustrata la definizione di utenti e gruppi nell'API di gestione autorizzazioni.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Utenti e gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319396"
---
# <a name="users-and-groups"></a>Utenti e gruppi

In Gestione autorizzazioni, i destinatari dei criteri di autorizzazione sono rappresentati dai gruppi seguenti:

-   Utenti e gruppi di Windows

    Questi gruppi includono utenti, computer e gruppi predefiniti per le entità di sicurezza.

-   Gruppi di query LDAP

    L'appartenenza a questi gruppi viene calcolata in modo dinamico in base alle esigenze delle query LDAP (Lightweight Directory Access Protocol). Un gruppo di query LDAP è un tipo di gruppo di applicazioni.

-   Gruppi di applicazioni di base

    Questi gruppi sono costituiti da gruppi di query LDAP, utenti e gruppi di Windows e altri gruppi di applicazioni di base.

## <a name="windows-users-and-groups"></a>Utenti e gruppi di Windows

Questi sono gli stessi utenti e gruppi utilizzati in tutto il sistema operativo Windows.

## <a name="ldap-query-groups"></a>Gruppi di query LDAP

In Gestione autorizzazioni è possibile utilizzare le query LDAP in modo che corrispondano agli attributi dell'utente con quelli dell'oggetto dell'utente in Active Directory.

Ad esempio, la query seguente trova tutti tranne Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



La query seguente consente di trovare tutti i membri dell'alias di un utente in www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Gruppi di applicazioni di base

Nell'API di gestione autorizzazioni, un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) . Un gruppo di applicazioni di base è un tipo di gruppo di applicazioni.

Per definire l'appartenenza a un gruppo di applicazioni di base, definire chi è un membro e definire chi non è un membro. Entrambi questi passaggi vengono eseguiti nello stesso modo. Specificare zero o più utenti e gruppi di Windows, gruppi di applicazioni di base definiti in precedenza o gruppi di query LDAP. L'appartenenza del gruppo di applicazioni di base viene calcolata rimuovendo tutti i membri non appartenenti al gruppo. Gestione autorizzazioni esegue questa operazione automaticamente in fase di esecuzione.

Il non membro di un gruppo di applicazioni di base ha la precedenza sull'appartenenza.

Le definizioni di appartenenza circolari non sono consentite. generano il messaggio di errore seguente: "Impossibile aggiungere GroupName. Si è verificato il seguente problema: è stato rilevato un ciclo ".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



