---
title: Riferimenti (ADSI)
description: Le segnalazioni si verificano quando il server su cui si esegue una query non contiene i dati, ma è in grado di trovarli.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Riferimenti ADSI
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

Le segnalazioni si verificano quando il server su cui si esegue una query non contiene i dati, ma è in grado di trovarli. Il server di destinazione restituisce il set di risultati, che può includere sia i dati effettivi che un riferimento a un altro server per recuperare i dati aggiuntivi. Abilitando *la ricerca delle* segnalazioni, il codice client ADSI sottostante userà i dati di riferimento per tentare di recuperare l'oggetto di destinazione dal server descritto nei dati di riferimento. Tenere presente che la disabilitazione della ricerca delle segnalazioni può comportare un set di risultati più piccolo, mentre l'abilitazione della ricerca dei riferimenti può causare l'esecuzione di una query su più server. Quando possibile, la soluzione consigliata consiste nell'usare il catalogo globale.

Per altre informazioni sulle segnalazioni e la ricerca di riferimenti in Active Directory, vedere [Segnalazioni](/windows/desktop/AD/referrals).

Ad esempio, quando un client indica al server A (A) di eseguire una query su un oggetto utente (U), A può suggerire che il client continui la ricerca nel Server B (B) se U non risiede in A, ma è noto che si trova in B. Il client può scegliere se proseguire o meno la segnalazione. Le segnalazioni di ricerca liberano il client dalla necessità di un riconoscimento avanzato della funzionalità di ogni server. Tuttavia, il client deve specificare il tipo di segnalazioni che un server deve effettuare.

Active Directory offre servizi di riferimento alla ricerca. Un client può scegliere uno dei tipi seguenti di ricerca delle segnalazioni:

-   Mai: il server non deve generare un riferimento a un client anche se riconosce che un altro server archivia i dati richiesti.
-   Esterno: il server deve generare riferimenti se la richiesta può essere risolta in un altro server di un albero di directory diverso. Ad esempio, un client esegue una query su "OU=Sales,DC=Fabrikam,DC=COM" nel server "fab01" nel dominio "Fabrikam.com". Tuttavia, l'oggetto non appartiene a "fab01", ma è noto per essere nel server "arc01" nel dominio "Fabrikam.com". Pertanto, "fab01" fa riferimento al client a "arc01".
-   Subordinato: il server deve generare riferimenti se la richiesta può essere risolta in un server il cui nome forma un percorso contiguo dal server di origine. L'ambito di ricerca deve essere a livello di sottoalbero.

    Ad esempio, il server A contiene oggetti in "DC=Sales,DC=Fabrikam,DC=Com". Il server B contiene oggetti in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=Com". Tenere presente che il nome del server B forma un percorso contiguo dal server A. Quando un client contatta il server A, richiede una ricerca nel sottoalbero in "DC=Sales,DC=Fabrikam,DC=Com" e specifica che la segnalazione è un tipo subordinato, si verifica l'evento seguente:

    -   Il server A restituisce tutti gli oggetti noti all'interno del relativo ambito.
    -   Il server A informa il client che gli oggetti in "DC=Seattle,DC=Sales,DC=Fabrikam,DC=COM" sono disponibili nel server B.

    Il client può scegliere di contattare il server B. In tal caso, si verifica l'evento seguente:

    -   Il server B risponde con gli oggetti richiesti.
    -   Se il server B rileva altri server nel percorso di denominazione contiguo e il processo continua.

-   Sempre: il server genera riferimenti se la ricerca può essere risolta in base al tipo esterno o al tipo subordinato.

> [!Note]  
> In Active Directory il catalogo globale contiene tutti gli oggetti in una determinata organizzazione. La ricerca di un server di catalogo globale produce prestazioni migliori rispetto all'esecuzione delle segnalazioni da un server a un altro.

 

Nella maggior parte dei casi, la ricerca delle segnalazioni sarà trasparente per il chiamante. Se la segnalazione è a un oggetto in un dominio o una foresta diversa, l'API LDAP sottostante tenterà di usare le credenziali correnti per l'associazione alla destinazione della segnalazione. Se l'operazione ha esito positivo, la ricerca delle segnalazioni sarà trasparente. Se l'operazione non riesce, verranno restituiti il codice di segnalazione e un codice di errore di segnalazione.

Per altre informazioni sull'uso delle opzioni di ricerca delle segnalazioni con un'interfaccia di ricerca specifica, vedere:

-   [Ricerca delle segnalazioni con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 