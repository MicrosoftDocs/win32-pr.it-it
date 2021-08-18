---
description: Gli intermediari comunicano con le applicazioni client per consentire loro di inviare richieste di certificato e (presupponendo che la richiesta abbia come risultato un certificato emesso) scaricare il certificato emesso nel client.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: Intermediari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f9dbd48d5af575658c04760740ad0b1f64f373d76bb20ba80253b874c67de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005289"
---
# <a name="intermediaries"></a>Intermediari

Gli intermediari comunicano con le [](../secgloss/c-gly.md)applicazioni client per consentire loro di inviare richieste di certificato e (presupponendo che la richiesta abbia come risultato un certificato emesso) per scaricare il certificato emesso nel client. Ogni protocollo del livello di trasporto richiede un proprio intermediario.

Servizi certificati Microsoft viene fornito con un intermediario (le pagine di registrazione Web) per HTTP. Un altro esempio di intermediario è lo snap-in MMC Microsoft Windows Certificates (che consente di richiamare la Richiesta guidata certificato). Se altri protocolli del livello di trasporto devono essere usati con Servizi certificati, uno sviluppatore può creare un intermediario per ogni protocollo del livello di trasporto desiderato.

Gli intermediari comunicano con Servizi certificati usando [**le interfacce ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) fornite dal motore server. Il [**metodo ICertRequest::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) viene [](../secgloss/c-gly.md)usato per inviare una richiesta di certificato e [**ICertRequest::GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) viene usato per ottenere il certificato emesso risultante. Analogamente, [**ICertConfig::GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) viene usato per determinare quale autorità di certificazione può essere usata per rilasciare il certificato.

Un intermediario non dipende dalla lingua. Può trattarsi di un programma scritto in C++, Visual Basic, Java, script o un altro linguaggio.

Oltre a raccogliere dati dal client per compilare una richiesta di certificato, un intermediario può specificare gli attributi della richiesta. Le richieste inviate [*a*](../secgloss/c-gly.md) un'autorità di certificazione che esegue il modulo dei criteri aziendali devono indicare il tipo di certificato richiesto specificando un attributo "CertificateTemplate" o un'estensione modello di certificato nella richiesta stessa.

Si noti che durante la creazione di una richiesta di certificato, gli sviluppatori (e gli intermediari) sono responsabili della gestione del segreto della chiave privata. Dopo che una chiave privata è stata compromessa (ha perso la segretezza), è inutile.

Le pagine di registrazione Web di Servizi certificati usano le interfacce di [registrazione certificati](cryptography-interfaces.md), che protegge le chiavi private generandole nella workstation. Oltre a mantenere la segretezza della chiave privata, il controllo di registrazione certificati consente a un intermediario di specificare il provider del servizio di crittografia, la specifica della chiave, l'intensità della chiave e l'algoritmo hash.

Lo snap-in MMC Certificati usa anche il controllo registrazione certificati (Xenroll.dll). Tuttavia, se le pagine di registrazione Web di Servizi certificati determinano il download della risorsa Controllo registrazione certificati (Xenroll.dll) nel client, se necessario, lo snap-in MMC Certificati viene eseguito in un ambiente in cui Xenroll.dll è già una risorsa disponibile.

Oltre a [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig,**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)gli sviluppatori [](cryptography-interfaces.md) di intermediari possono [](certificate-enrollment-control.md) trovare utili le interfacce di registrazione certificati e il controllo di registrazione smart card.

 

 
