---
description: Un'autorità di certificazione (CA) è responsabile dell'attestazione dell'identità di utenti, computer e organizzazioni.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Autorità di certificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5f48c897c74e5f0bf7d4d3b1e21b8f89d33e72cdfa46aefe726f714fbc267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904500"
---
# <a name="certification-authorities"></a>Autorità di certificazione

[*Un'autorità*](/windows/desktop/SecGloss/c-gly) di certificazione (CA) è responsabile dell'attestazione dell'identità di utenti, computer e organizzazioni. La CA autentica un'entità e convalida l'identità mediante il rilascio in un certificato firmato digitalmente. La CA può inoltre gestire, revocare e rinnovare i certificati.

Una CA può essere pubblica o privata. Una CA pubblica fornisce servizi di certificazione, in genere a pagamento, al pubblico tramite Internet. Una CA privata fornisce questo servizio ai membri di una popolazione delimitata, ad esempio i dipendenti di un'azienda o i membri di un altro gruppo privato.

I mezzi con cui una CA autentica un utente finale sono diversi e oltre l'ambito di questa documentazione. Chiaramente, tuttavia, i metodi di autenticazione variano in base al tipo di provider. Ad esempio, una CA privata può stabilire l'identità degli utenti finali facendo riferimento a un elenco di gruppi, ad esempio un database dipendente o Active Directory. I metodi di autenticazione eseguiti da una CA pubblica sono in genere più complessi e dipendono in parte dal livello di garanzia promessa dal certificato.

Con l'aumentare della popolazione di un'infrastruttura a chiave pubblica (PKI), può diventare difficile per una singola CA gestire in modo efficace tutti i certificati emessi. La CA può compensare autorizzando altre CA nell'infrastruttura a chiave pubblica (PKI) a rilasciare certificati. La CA iniziale è denominata radice e le CA che autorizza sono denominate subordinate. Le autorità di certificazione subordinate possono anche designare le proprie filiali entro i limiti impostati dalla radice. La struttura risultante è denominata gerarchia di certificati. I certificati rilasciati alle AUTORITÀ di certificazione inferiori nella gerarchia contengono certificati sufficienti per tracciare un percorso alla radice. Si tratta di una catena di certificati.

Il termine autorità di certificazione può fare riferimento sia all'organizzazione che garantisce l'identità di un utente finale che al server utilizzato dall'organizzazione per rilasciare e gestire i certificati. Un Windows server può essere configurato per fungere da server CA e questa documentazione si riferisce in genere al server quando si usa il termine CA.

L'API Di registrazione certificati interagisce principalmente con una CA usando [**l'oggetto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) Il [**metodo Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) per questo oggetto può codificare automaticamente una richiesta di certificato, inviarla alla CA e installare il certificato emesso. È anche possibile usare un oggetto **IX509Enrollment** inizializzato per la registrazione fuori banda o per la registrazione ritardata. È anche possibile usare l'oggetto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) per monitorare lo stato della registrazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 
