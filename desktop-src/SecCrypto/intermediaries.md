---
description: Gli intermediari comunicano con le applicazioni client per consentire loro di inviare richieste di certificato e (presupponendo che la richiesta abbia come risultato un certificato emesso) per scaricare il certificato emesso nel client.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: Intermediari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320506"
---
# <a name="intermediaries"></a>Intermediari

Gli intermediari comunicano con le applicazioni client per consentire loro di inviare [*richieste di certificato*](../secgloss/c-gly.md)e (presupponendo che la richiesta abbia come risultato un certificato emesso) per scaricare il certificato emesso nel client. Ogni protocollo del livello di trasporto richiede un proprio intermediario.

Servizi certificati Microsoft viene fornito con un intermediario (pagine di registrazione Web) per HTTP. Un altro esempio di intermediario è lo snap-in MMC certificati di Microsoft Windows (che consente di richiamare la richiesta guidata certificato). Se è necessario utilizzare altri protocolli del livello di trasporto con servizi certificati, uno sviluppatore può creare un intermediario per ogni protocollo di livello trasporto desiderato.

Gli intermediari comunicano con i servizi certificati usando le interfacce [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) fornite dal motore del server. Il metodo [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) viene usato per inviare una [*richiesta di certificato*](../secgloss/c-gly.md)e [**ICertRequest:: GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) viene usato per ottenere il certificato emesso risultante. Analogamente, [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) viene usato per determinare quale autorità di certificazione può essere usata per emettere il certificato.

Un intermediario non dipende dalla lingua. Potrebbe trattarsi di un programma scritto in C++, Visual Basic, Java, script o in un altro linguaggio.

Oltre a raccogliere i dati dal client per compilare una richiesta di certificato, un intermediario può specificare gli attributi della richiesta. Le richieste inviate a un' [*autorità di certificazione*](../secgloss/c-gly.md) che esegue il modulo criteri di organizzazione devono indicare il tipo di certificato richiesto specificando un attributo "CertificateTemplate" o un'estensione del modello di certificato nella richiesta stessa.

Si noti che durante la creazione di una richiesta di certificato, gli sviluppatori (e gli intermediari) sono responsabili del mantenimento della segretezza della chiave privata. Dopo che una chiave privata è stata compromessa (perso il segreto), è inutile.

Le pagine di registrazione Web di Servizi certificati utilizzano le [interfacce di registrazione certificati](cryptography-interfaces.md), che proteggono le chiavi private generando tali interfacce sulla workstation. Oltre a mantenere la segretezza della chiave privata, il controllo di registrazione dei certificati consente a un intermediario di specificare il provider del servizio di crittografia, la specifica della chiave, il livello di attendibilità della chiave e l'algoritmo hash.

Lo snap-in MMC certificati USA anche il controllo di registrazione certificati (Xenroll.dll). Tuttavia, in cui le pagine di registrazione Web di Servizi certificati comportano il download della risorsa di controllo di registrazione del certificato (Xenroll.dll) nel client, se necessario, lo snap-in MMC certificati viene eseguito in un ambiente in cui Xenroll.dll è già una risorsa disponibile.

Oltre a [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig), gli sviluppatori di intermediari possono trovare le interfacce di [registrazione del certificato](cryptography-interfaces.md) e il controllo di [registrazione delle smart card](certificate-enrollment-control.md) per essere utile.

 

 
