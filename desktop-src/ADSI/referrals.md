---
title: Riferimenti (ADSI)
description: I riferimenti si verificano quando il server su cui si esegue una query non contiene tali dati, ma è possibile trovarli.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- Riferimenti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118439"
---
# <a name="referrals-adsi"></a>Riferimenti (ADSI)

I riferimenti si verificano quando il server su cui si esegue una query non contiene tali dati, ma è possibile trovarli. Il server di destinazione restituisce il set di risultati, che può includere sia i dati effettivi che un riferimento a un altro server per recuperare i dati aggiuntivi. Abilitando la ricerca dei *riferimenti*, il codice client ADSI sottostante utilizzerà i dati di riferimento per tentare di recuperare l'oggetto di destinazione dal server descritto nei dati di riferimento. Tenere presente che la disabilitazione della ricerca dei riferimenti può comportare un set di risultati più piccolo, mentre l'abilitazione del riferimento può causare la disattivazione di una query su più server. Quando possibile, la soluzione consigliata consiste nell'usare il catalogo globale.

Per ulteriori informazioni sui riferimenti e l'inseguimento dei riferimenti in Active Directory, vedere [riferimenti](/windows/desktop/AD/referrals).

Ad esempio, quando un client indica al server A (A) di eseguire una query su un oggetto utente (U), un può suggerire che il client continua la ricerca nel server B (B) se U non si trova in un, ma è noto come B. Il client ha la possibilità di scegliere di seguire o meno il riferimento. I riferimenti di ricerca fanno in modo che il client richieda un riconoscimento avanzato della funzionalità di ogni server. Tuttavia, il client deve specificare il tipo di riferimenti che un server deve eseguire.

Active Directory offre servizi di riferimento per la ricerca. Un client può scegliere uno dei seguenti tipi di Chasing di riferimento:

-   Mai: il server non deve generare un riferimento a un client anche se riconosce che un altro server archivia i dati richiesti.
-   Esterno: il server deve generare riferimenti se la richiesta può essere risolta in un altro server di un albero di directory diverso. Ad esempio, un client esegue una query "OU = Sales, DC = Fabrikam, DC = COM" nel server "fab01" nel dominio "Fabrikam.com". Tuttavia, l'oggetto non appartiene a "fab01", ma è noto che si trova nel server "ARC01" nel dominio "Fabrikam.com". Quindi, "fab01" fa riferimento al client a "ARC01".
-   Subordinata: il server deve generare riferimenti se la richiesta può essere risolta in un server il cui nome costituisce un percorso contiguo dal server di origine. L'ambito di ricerca deve essere a livello di sottoalbero.

    Ad esempio, il server A contiene oggetti in "DC = Sales, DC = Fabrikam, DC = com". Il server B contiene oggetti in "DC = Seattle, DC = Sales, DC = Fabrikam, DC = com". Tenere presente che il nome del server B costituisce un percorso contiguo dal server A. Quando un client contatta il server A, richiede la ricerca di un sottoalbero su "DC = Sales, DC = Fabrikam, DC = com" e specifica che il riferimento deve essere un tipo subordinato, si verifica l'evento seguente:

    -   Il server A restituisce tutti gli oggetti che conosce nell'ambito.
    -   Il server A informa il client che gli oggetti in "DC = Seattle, DC = Sales, DC = Fabrikam, DC = COM" sono reperibili nel server B.

    Il client può scegliere di contattare il server B. In tal caso, si verifica l'evento seguente:

    -   Il server B risponde con gli oggetti richiesti.
    -   Se il server B rileva altri server nel percorso di denominazione contiguo e il processo continua.

-   Sempre: il server genera riferimenti se la ricerca può essere risolta in base al tipo esterno o al tipo subordinato.

> [!Note]  
> In Active Directory, il catalogo globale contiene tutti gli oggetti in una determinata azienda. La ricerca di un server di catalogo globale garantisce prestazioni migliori rispetto al proseguimento dei riferimenti da un server a un altro.

 

Nella maggior parte dei casi, l'inseguimento dei riferimenti sarà trasparente per il chiamante. Se il riferimento è a un oggetto in un dominio o in una foresta diversa, l'API LDAP sottostante tenterà di usare le credenziali correnti per eseguire il binding alla destinazione del riferimento. Se l'operazione ha esito positivo, l'inseguimento dei riferimenti sarà trasparente. Se l'operazione non riesce, verrà restituito il riferimento e un codice di errore di riferimento.

Per ulteriori informazioni sull'utilizzo delle opzioni di ricerca dei riferimenti con un'interfaccia di ricerca specifica, vedere:

-   [Inseguimento dei riferimenti con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 