---
description: Una piattaforma di sviluppo per la creazione di autorità di certificazione per le aziende o per applicazioni Internet sicure.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Architettura di Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b7e0545b2f0fe0dd8c30d1863ffdf52c64a9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226351"
---
# <a name="certificate-services-architecture"></a>Architettura di Servizi certificati

Servizi certificati è una piattaforma di sviluppo per la creazione di autorità di certificazione per le aziende o per applicazioni Internet sicure. Un'autorità di certificazione configurata e operativa consentirà a un sito di emettere, rilevare, gestire e revocare i certificati con un sovraccarico minimo di amministrazione e la massima sicurezza.

I servizi certificati sono costituiti dal motore Server, dal database del server e da un set di moduli e strumenti che interagiscono tra loro per fungere da autorità di certificazione. Le applicazioni, i moduli e gli strumenti di amministrazione esterni utilizzano le interfacce Component Object Model (COM) per interagire con il motore del server. Il diagramma seguente illustra le interfacce usate dal motore del server:

![architettura di Servizi certificati](images/certapi.png)

Un sistema di certificazione operativo in genere avrà quattro sottosistemi principali.



| Subsystem             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client                | Il client è il software usato dall'utente finale per generare una [*richiesta di certificato*](../secgloss/c-gly.md), inviare la richiesta e ricevere il certificato terminato. Un esempio di client è Microsoft Internet Explorer versione 5. Il client interagirà in genere con un'interfaccia personalizzata gestita dall'applicazione intermediario.                                                                                                                                                                                                                                                                                              |
| Intermediario          | L'intermediario è un sottosistema costituito dall'applicazione intermedia e dall'interfaccia client dei servizi certificati (*client Web di Servizi certificati* nel programma di installazione di). L'applicazione intermedia interagisce direttamente con il client, ricevendo richieste di certificati e restituendo i certificati completati. Comunica con il motore del server tramite l'interfaccia client di Servizi certificati, che contiene le interfacce COM [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) e [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) . Un esempio di applicazione intermedia è Microsoft Internet Information Services. L'applicazione intermedia può essere implementata interamente tramite Active Server pagine. |
| Server                | Il server è il sistema che compila il certificato. Oltre al motore del server, sono inclusi due componenti configurabili; il modulo criteri e il modulo di uscita. Il modulo criteri interagisce con il motore del server tramite le interfacce [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Uscire dai moduli (possono essere presenti più di uno) interagire con il motore del server tramite le interfacce [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) e [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) .                                                                                                                                                                                       |
| Client amministrativo | Il client di amministrazione è il sistema che monitora e gestisce certificati e richieste. Il client amministrativo utilizza l'interfaccia [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) per comunicare con il motore del server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Per ulteriori informazioni sull'architettura di Servizi certificati, vedere [interfacce di crittografia](cryptography-interfaces.md), [compilazione di un certificato](building-a-certificate.md)e gli argomenti seguenti.



| Sezione                                      | Content                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Moduli criteri](policy-modules.md)         | Programmi personalizzabili che possono essere usati durante la valutazione delle [*richieste di certificati*](../secgloss/c-gly.md); questi programmi applicano le regole in base alle quali servizi certificati rilascia o nega la richiesta. |
| [Moduli di uscita](exit-modules.md)             | Programmi personalizzabili che ricevono notifiche dal motore del server quando si verificano le operazioni, ad esempio quando viene emesso un certificato.                                                                                                                                       |
| [Gestori estensioni](extension-handlers.md) | Oggetti COM che forniscono routine per la codifica di estensioni e tipi di dati più complessi.                                                                                                                                                                                 |
| [Intermediari](intermediaries.md)         | Programmi che comunicano con le applicazioni client per consentire l'invio di richieste di certificati.                                                                                                                                                                        |



 

 

 
