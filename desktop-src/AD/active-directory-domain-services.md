---
title: Servizi di dominio di Active Directory
description: Microsoft Active Directory Domain Services sono la base per le reti distribuite basate sui sistemi operativi Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 che usano i controller di dominio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, pagina iniziale
- Active Directory Domain Services Active Directory, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047564"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>Scopo

Microsoft Active Directory Domain Services sono la base per le reti distribuite basate sui sistemi operativi Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 che usano i controller di dominio. Active Directory Domain Services offrono archiviazione dati gerarchica e sicura, strutturata, per gli oggetti in una rete, ad esempio utenti, computer, stampanti e servizi. Active Directory Domain Services fornire supporto per l'individuazione e l'utilizzo di questi oggetti.

Questa guida fornisce una panoramica dell'Active Directory Domain Services e del codice di esempio per le attività di base, ad esempio la ricerca di oggetti e la lettura delle proprietà, per attività più avanzate, ad esempio la pubblicazione del servizio.

Windows 2000 Server e i sistemi operativi successivi forniscono un'interfaccia utente che consente a utenti e amministratori di utilizzare gli oggetti e i dati in Active Directory Domain Services. Questa guida descrive come estendere e personalizzare l'interfaccia utente. Viene inoltre descritto come estendere Active Directory Domain Services definendo nuove classi di oggetti e attributi.

> [!Note]  
> La documentazione seguente è destinata ai programmatori di computer. Se si è un utente finale che tenta di eseguire il debug di un errore di stampa o di una rete domestica, vedere i [Forum della community Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Se applicabile

Gli amministratori di rete scrivono gli script e le applicazioni che accedono Active Directory Domain Services per automatizzare le attività amministrative comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.

I fornitori di software indipendenti e gli sviluppatori di utenti finali possono utilizzare la programmazione Active Directory Domain Services per abilitare la directory di prodotti e applicazioni. I servizi possono essere pubblicati in Active Directory Domain Services; i client possono utilizzare Active Directory Domain Services per trovare i servizi ed entrambi possono utilizzare Active Directory Domain Services per individuare e utilizzare altri oggetti in una rete.

## <a name="developer-audience"></a>Sviluppatori

Le applicazioni che accedono ai dati in Active Directory Domain Services possono essere scritte usando l'API [interfacce del servizio Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , l'API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) o lo spazio dei nomi [System. DirectoryServices](/dotnet/api/system.directoryservices) .

## <a name="run-time-requirements"></a>Requisiti di runtime

Active Directory Domain Services eseguiti nei controller di dominio Windows 2000 e versioni successive. Tuttavia, le applicazioni client possono essere scritte ed eseguite in Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 e Windows 95.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Informazioni su Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Informazioni generali sulla Active Directory Domain Services.

</dd> <dt>

[Uso di Active Directory Domain Services](using-active-directory-domain-services.md)
</dt> <dd>

Guida alla programmazione Active Directory Domain Services.

</dd> <dt>

[Riferimento Active Directory Domain Services](active-directory-domain-services-reference.md)
</dt> <dd>

Riferimento alla programmazione Active Directory Domain Services.

</dd> </dl>

 

 