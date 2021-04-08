---
description: Considerazioni sulla sicurezza del servizio SOAP COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Considerazioni sulla sicurezza del servizio SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878278"
---
# <a name="com-soap-service-security-considerations"></a>Considerazioni sulla sicurezza del servizio SOAP COM+

Il servizio SOAP COM+ dipende dal server Web IIS per la sicurezza. Anche in [modalità oggetto attivato dal client](accessing-xml-web-services-in-cao-mode.md), una RPC com+ non trasmette l'identità del client e pertanto non può utilizzare la protezione basata sui ruoli o qualsiasi altra funzionalità di sicurezza fornita da DCOM. Per proteggere la privacy dei dati trasmessi da e verso il servizio Web XML o per proteggere il servizio Web XML da accessi non autorizzati, è possibile configurare IIS per limitare l'accesso a un servizio Web XML in base a un indirizzo IP dei client o richiedere a un client di presentare un certificato digitale per verificarne l'identità. Se non si limita l'accesso, qualsiasi client in grado di comunicare con il server Web può accedere al servizio Web XML.

È possibile configurare IIS per crittografare le comunicazioni del servizio Web XML con i client usando i protocolli SSL o TLS per la crittografia a chiave pubblica. Se non si crittografano le comunicazioni SOAP, i dati scambiati tra un client e un server possono essere osservati da terze parti con accesso a qualsiasi rete in cui la comunicazione SOAP viene spostata; a seconda della topologia di rete, potrebbe trattarsi di una piccola LAN o Internet.

Per impostazione predefinita, le comunicazioni SOAP non crittografate vengono ricevute sulla porta HTTP (80) e le comunicazioni SOAP crittografate vengono ricevute sulla porta HTTPS (443). Affinché un client riesca ad accedere a un servizio Web XML, è necessario configurare tutti i firewall tra il client e il server per consentire ai pacchetti SYN TCP di raggiungere la porta del server appropriata. Viceversa, per limitare l'accesso ai servizi Web XML, un amministratore del firewall può scegliere di chiudere queste porte.

Le impostazioni di sicurezza predefinite per un componente COM esposto come un servizio Web XML variano a seconda della versione di Microsoft .NET Framework installata. Se è installata la versione 1,0, i servizi Web XML non sono protetti per impostazione predefinita. tutte le chiamate vengono accettate e non viene utilizzata alcuna crittografia. Se è installata la versione 1,1 o una versione successiva, i servizi Web XML sono protetti per impostazione predefinita. i chiamanti devono essere autenticati e la crittografia è obbligatoria.

Un servizio Web XML protetto non supporta l'accesso WKO tramite WSDL. I client che hanno installato la versione di .NET Framework 1,1 possono invece chiamarlo in modalità CAO. Se i client di terze parti devono accedere al servizio Web XML tramite WSDL, è necessario consentire l'accesso anonimo.

Un componente COM esposto come servizio Web XML viene eseguito per impostazione predefinita con le autorizzazioni dell'utente anonimo, non con le autorizzazioni del chiamante. È possibile configurare IIS per eseguire il servizio Web XML come utente diverso. Questa operazione può talvolta essere necessaria perché il componente utilizza file o altre risorse a cui l'utente anonimo non ha accesso. Tuttavia, è consigliabile provare sempre a eseguire il componente con il minor numero possibile di privilegi, per limitare il danno che può causare un chiamante dannoso.

> [!Note]  
> Poiché un metodo esposto tramite un servizio Web XML potrebbe essere potenzialmente esposto a chiamanti dannosi, è sempre necessario assicurarsi di convalidare i parametri di input da cui dipende.

 

Per istruzioni dettagliate su come configurare specifiche impostazioni di sicurezza del servizio Web XML, vedere [protezione di servizi Web XML](securing-xml-web-services.md).

**Per convertire un'applicazione SOAP protetta in un'applicazione SOAP non protetta**

1.  Aprire lo strumento di amministrazione Internet Information Services (IIS).
2.  Individuare la directory virtuale per l'applicazione e aprire la finestra di dialogo **Proprietà** .
3.  Selezionare **Abilita la pagina contenuto predefinito** nella scheda **documenti** .
4.  Nella scheda **sicurezza directory** fare clic su **modifica** in **accesso anonimo e controllo autenticazione**.
5.  Controllare **l'accesso anonimo** per abilitare l'accesso anonimo e fare clic su **OK**.
6.  Fare clic su **modifica** in **comunicazioni sicure**.
7.  Deselezionare la casella di controllo **Richiedi canale sicuro (SSL)** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> </dl>

 

 



