---
title: Riferimenti (ADSI)
description: Le segnalazioni si verificano quando il server su cui si esegue una query non contiene i dati, ma è in grado di trovarli.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Segnalazioni ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5fb6ad299c2f47efa9723857b53cf7eee5350589757153eaaae869b2c37e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444021"
---
# <a name="referrals-adsi"></a>Riferimenti (ADSI)

Le segnalazioni si verificano quando il server su cui si esegue una query non contiene i dati, ma è in grado di trovarli. Il server di destinazione restituisce il set di risultati, che può includere sia i dati effettivi che un riferimento a un altro server per recuperare i dati aggiuntivi. Abilitando *la ricerca dei riferimenti,* il codice client ADSI sottostante userà i dati di riferimento per tentare di recuperare l'oggetto di destinazione dal server descritto nei dati di riferimento. Tenere presente che la disabilitazione della ricerca di riferimenti può comportare un set di risultati più piccolo, mentre l'abilitazione della ricerca di riferimenti può causare l'estensione di una query a più server. Quando possibile, la soluzione consigliata consiste nell'usare il catalogo globale.

Per altre informazioni sulle segnalazioni e sulla ricerca di segnalazioni in Active Directory, vedi [Segnalazioni.](/windows/desktop/AD/referrals)

Ad esempio, quando un client indica al Server A (A) di eseguire una query su un oggetto utente (U), A può suggerire che il client continui la ricerca nel Server B (B) se U non risiede in A, ma è noto come in B. Il client ha la possibilità di scegliere se o meno la segnalazione. Le segnalazioni di ricerca non richiedono al client il riconoscimento avanzato della funzionalità di ogni server. Tuttavia, il client deve specificare il tipo di riferimenti che un server deve eseguire.

Active Directory offre servizi di segnalazione della ricerca. Un client può scegliere uno dei tipi seguenti di ricerca dei riferimenti:

-   Mai: il server non deve generare un riferimento a un client anche se riconosce che un altro server archivia i dati richiesti.
-   Esterno: il server deve generare riferimenti se la richiesta può essere risolta in un altro server di un albero di directory diverso. Ad esempio, un client esegue una query su "OU=Sales,DC=Fabrikam,DC=COM" sul server "fab01" nel dominio "Fabrikam.com". Tuttavia, l'oggetto non appartiene a "fab01", ma è noto per essere nel server "arc01" nel dominio "Fabrikam.com". Pertanto, "fab01" fa riferimento al client a "arc01".
-   Subordinato: il server deve generare riferimenti se la richiesta può essere risolta in un server il cui nome forma un percorso contiguo dal server di origine. L'ambito di ricerca deve essere a livello di sottoalbero.

    Ad esempio, il Server A contiene oggetti in "DC=Sales,DC=Fabrikam,DC=Com". Il server B contiene oggetti in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=Com". Tenere presente che il nome del Server B forma un percorso contiguo dal Server A. Quando un client contatta il Server A, richiede una ricerca nel sottoalbero in "DC=Sales,DC=Fabrikam,DC=Com" e specifica che il riferimento deve essere un tipo subordinato, si verifica l'evento seguente:

    -   Il server A restituisce tutti gli oggetti noti all'interno del relativo ambito.
    -   Il server A informa il client che gli oggetti in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=COM" sono disponibili nel Server B.

    Il client può scegliere di contattare il Server B. In tal caso, si verifica l'evento seguente:

    -   Il server B risponde con gli oggetti richiesti.
    -   Se il Server B rileva altri server nel percorso di denominazione contiguo e il processo continua.

-   Sempre: il server genera riferimenti se la ricerca può essere risolta in base al tipo esterno o al tipo subordinato.

> [!Note]  
> In Active Directory, il catalogo globale contiene tutti gli oggetti in una determinata organizzazione. La ricerca in un server di catalogo globale produce prestazioni migliori rispetto all'esecuzione di riferimenti da un server a un altro.

 

Nella maggior parte dei casi, la ricerca delle segnalazioni sarà trasparente per il chiamante. Se il riferimento è a un oggetto in un dominio o in una foresta diversa, l'API LDAP sottostante tenterà di usare le credenziali correnti per l'associazione alla destinazione della segnalazione. Se l'operazione ha esito positivo, la ricerca delle segnalazioni sarà trasparente. Se l'operazione non riesce, verranno restituiti la segnalazione e un codice di errore di segnalazione.

Per altre informazioni sull'uso delle opzioni di ricerca delle segnalazioni con un'interfaccia di ricerca specifica, vedere:

-   [Ricerca di riferimenti con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 