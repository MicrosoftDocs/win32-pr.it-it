---
description: Un'autorità di certificazione (CA) è responsabile dell'attestazione dell'identità di utenti, computer e organizzazioni.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Autorità di certificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883630"
---
# <a name="certification-authorities"></a>Autorità di certificazione

Un' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) è responsabile dell'attestazione dell'identità di utenti, computer e organizzazioni. La CA autentica un'entità e convalida l'identità mediante il rilascio in un certificato firmato digitalmente. La CA può inoltre gestire, revocare e rinnovare i certificati.

Una CA può essere pubblica o privata. Una CA pubblica fornisce servizi di certificazione, in genere per una tariffa, al pubblico tramite Internet. Una CA privata fornisce questo servizio ai membri di un popolamento delimitato, ad esempio i dipendenti di un'azienda o i membri di un altro gruppo privato.

Il modo in cui un'autorità di certificazione autentica un utente finale è vario e non rientra nell'ambito di questa documentazione. Ovviamente, tuttavia, i metodi di autenticazione variano in base al tipo di provider. Una CA privata, ad esempio, può stabilire l'identità degli utenti finali facendo riferimento a un roster del gruppo, ad esempio un database dei dipendenti o Active Directory. I metodi di autenticazione eseguiti da una CA pubblica sono in genere più complessi e dipendono in parte dal livello di garanzia promesso dal certificato.

Man mano che la popolazione di un'infrastruttura a chiave pubblica (PKI) cresce, può diventare difficile per una singola autorità di certificazione gestire efficacemente tutti i certificati emessi. La CA può compensare autorizzando altre CA nell'infrastruttura PKI a emettere certificati. La CA iniziale viene chiamata radice e le autorità di certificazione autorizzate sono denominate subordinate. Le CA subordinate possono anche designare le proprie filiali entro i limiti impostati dalla radice. La struttura risultante è detta gerarchia di certificati. I certificati rilasciati a CAs inferiori nella gerarchia contengono un numero sufficiente di certificati per tracciare un percorso alla radice. Questa operazione è denominata catena di certificati.

Il termine autorità di certificazione può fare riferimento sia all'organizzazione che garantisce l'identità di un utente finale che al server usato dall'organizzazione per rilasciare e gestire i certificati. Un server Windows può essere configurato in modo da fungere da server CA e questa documentazione si riferisce in genere al server quando si usa il termine CA.

L'API di registrazione del certificato interagisce con una CA principalmente usando l'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . Il metodo di [**registrazione**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) in questo oggetto può codificare automaticamente una richiesta di certificato, inviarla all'autorità di certificazione e installare il certificato emesso. È anche possibile usare un oggetto **metodo IX509Enrollment** inizializzato per la registrazione fuori banda o per la registrazione ritardata. Inoltre, è possibile usare l'oggetto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) per monitorare lo stato di registrazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 
