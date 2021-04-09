---
title: Binding a Active Directory Domain Services
description: In Active Directory Domain Services, l'operazione di associazione di un oggetto programmatico a un oggetto Active Directory Domain Services specifico è nota come binding.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- associazione a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965963"
---
# <a name="binding-to-active-directory-domain-services"></a>Binding a Active Directory Domain Services

In Active Directory Domain Services, l'operazione di associazione di un oggetto programmatico a un oggetto Active Directory Domain Services specifico è nota come *Binding*. Quando un oggetto a livello di codice, ad esempio un oggetto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , è associato a un oggetto directory specifico, l'oggetto programmatico viene considerato *associato* all'oggetto directory.

## <a name="binding-functions-and-methods"></a>Funzioni e metodi di associazione

Il metodo per l'associazione a livello di codice a un oggetto Active Directory dipenderà dalla tecnologia di programmazione utilizzata. Per ulteriori informazioni sull'associazione a oggetti in Active Directory Domain Services con una tecnologia di programmazione specifica, vedere gli argomenti elencati nella tabella seguente.



| Tecnologia di programmazione                                                                       | Per ulteriori informazioni                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Interfacce di servizio Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Associazione a un oggetto ADSI](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Creazione di una sessione LDAP](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Associazione a oggetti directory](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Binding di stringhe

Tutte le funzioni e i metodi di associazione richiedono una stringa di associazione. Il formato della stringa di associazione dipende dal provider. Active Directory Domain Services sono supportati da due provider, LDAP e WinNT.

A partire da Windows 2000, il provider LDAP viene usato per accedere Active Directory Domain Services. La stringa di binding LDAP può assumere uno dei seguenti formati:

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

Negli esempi precedenti, "LDAP:" specifica il provider LDAP. "GC:" utilizza il provider LDAP per l'associazione al servizio di catalogo globale per eseguire query veloci.

" &lt; nome host &gt; " specifica il server a cui eseguire il binding ed è facoltativo. Se possibile, non specificare un server. È anche possibile eseguire l'associazione a un oggetto in un dominio diverso. A tale scopo, passare il nome DNS (Domain Naming System) del dominio di destinazione per " &lt; host name &gt; ". Ad esempio, per eseguire l'associazione al contenitore Users nel dominio domain2 di fabrikam.com, la stringa di associazione sarà "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".

" &lt; nome oggetto &gt; " rappresenta un oggetto specifico in Active Directory Domain Services. Il nome dell'oggetto può essere un nome distinto o un GUID dell'oggetto.

Per ulteriori informazioni sulle stringhe di binding LDAP, vedere [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).

Per Windows NT 4,0, il provider WinNT viene usato per l'accesso ai dati della directory, ad esempio utenti, gruppi di utenti, computer, servizi e altri oggetti di rete in Windows 2000. Il provider WinNT nei sistemi Windows 2000 e versioni successive presenta funzionalità limitate rispetto al provider LDAP. Per ulteriori informazioni sulle stringhe di binding WinNT, vedere [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).

Per eseguire il binding alla radice dello spazio dei nomi, è possibile usare un ADsPath di "LDAP://" o "GC://". Quando viene associato alla radice dello spazio dei nomi, l'oggetto spazio dei nomi fornito non contiene proprietà e contiene l'oggetto dominio per LDAP e un oggetto contenitore contenente una replica parziale di tutti i domini nella foresta per GC.

Per ulteriori informazioni sull'associazione in Active Directory Domain Services, vedere:

-   [Binding senza server e RootDSE](serverless-binding-and-rootdse.md)
-   [Associazione al catalogo globale](binding-to-the-global-catalog.md)
-   [Utilizzo di objectGUID per l'associazione a un oggetto](using-objectguid-to-bind-to-an-object.md)
-   [Associazione a oggetti Well-Known mediante WKGUID](binding-to-well-known-objects-using-wkguid.md)
-   [Associazione a un oggetto tramite un SID](binding-to-an-object-using-a-sid.md)
-   [Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [autenticazione](authentication.md)

 

 
