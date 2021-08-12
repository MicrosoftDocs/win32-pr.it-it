---
description: Considerazioni sulla sicurezza dei servizi SOAP COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Considerazioni sulla sicurezza dei servizi SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67e034dfeaa4ec7f8688420aafcaec434653c942665ec3e3cbaa1535b51980d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548550"
---
# <a name="com-soap-service-security-considerations"></a>Considerazioni sulla sicurezza dei servizi SOAP COM+

Il servizio SOAP COM+ dipende dal server Web IIS per motivi di sicurezza. Anche in modalità oggetto attivata dal [client,](accessing-xml-web-services-in-cao-mode.md)una RPC COM+ non trasmette l'identità del client e pertanto non può usare la sicurezza basata sui ruoli o qualsiasi altra funzionalità di sicurezza fornita da DCOM. Se si desidera proteggere la privacy dei dati trasmessi da e verso il servizio Web XML o per proteggere il servizio Web XML da accessi non autorizzati, è possibile configurare IIS per limitare l'accesso a un servizio Web XML in base a un indirizzo IP del client o per richiedere a un client di presentare un certificato digitale per verificarne l'identità. Se non si limita l'accesso, qualsiasi client in grado di comunicare con il server Web può accedere al servizio Web XML.

È possibile configurare IIS per crittografare le comunicazioni del servizio Web XML con i client usando protocolli SSL o TLS di crittografia a chiave pubblica. Se non si crittografa le comunicazioni SOAP, i dati s scambiati tra un client e un server potrebbero essere osservati da terze parti con accesso a qualsiasi rete su cui si sposta la comunicazione SOAP; A seconda della topologia di rete, potrebbe trattarsi di una LAN di piccole dimensioni o di Internet.

Per impostazione predefinita, le comunicazioni SOAP non crittografate vengono ricevute sulla porta HTTP (80) e le comunicazioni SOAP crittografate vengono ricevute sulla porta HTTPS (443). Per consentire a un client di accedere correttamente a un servizio Web XML, tutti i firewall tra il client e il server devono essere configurati per consentire ai pacchetti SYN TCP di raggiungere la porta del server appropriata. Al contrario, per limitare l'accesso ai servizi Web XML, un amministratore del firewall può scegliere di chiudere queste porte.

Le impostazioni di sicurezza predefinite per un componente COM esposto come servizio Web XML variano a seconda della versione di Microsoft .NET Framework installata. Se è installata la versione 1.0, i servizi Web XML non sono protetti per impostazione predefinita. tutte le chiamate vengono accettate e non viene usata alcuna crittografia. Se è installata la versione 1.1 o successiva, i servizi Web XML sono protetti per impostazione predefinita. I chiamanti devono essere autenticati ed è necessaria la crittografia.

Un servizio Web XML protetto non supporta l'accesso WKO tramite WSDL. Al contrario, i client che hanno installato .NET Framework versione 1.1 possono chiamarlo in modalità CAO. Se i client di terze parti devono accedere al servizio Web XML tramite WSDL, è necessario consentire l'accesso anonimo.

Un componente COM esposto come servizio Web XML viene eseguito per impostazione predefinita con le autorizzazioni dell'utente anonimo (non con le autorizzazioni del chiamante). È possibile configurare IIS per eseguire il servizio Web XML come utente diverso. Questa operazione può talvolta essere necessaria perché il componente usa file o altre risorse a cui l'utente anonimo non ha accesso. Tuttavia, è consigliabile provare sempre a eseguire il componente con il numero più limitato possibile di privilegi, per limitare i danni che un chiamante malintenzionato potrebbe causare.

> [!Note]  
> Poiché un metodo esposto tramite un servizio Web XML potrebbe essere potenzialmente esposto a chiamanti dannosi, è sempre necessario assicurarsi di convalidare tutti i parametri di input da cui dipende.

 

Per istruzioni dettagliate su come configurare impostazioni di sicurezza del servizio Web XML specifiche, vedere [Protezione dei servizi Web XML.](securing-xml-web-services.md)

**Per convertire un'applicazione SOAP protetta in un'applicazione SOAP non protetta**

1.  Aprire lo Internet Information Services di amministrazione di Internet Information Services (IIS).
2.  Individuare la directory virtuale per l'applicazione e aprire la **finestra di dialogo** Proprietà .
3.  Selezionare **Abilita contenuto predefinito nella** **scheda** Documenti.
4.  Nella scheda **Sicurezza directory fare** clic su Modifica **in** Controllo autenticazione e **accesso anonimo**.
5.  Selezionare **Accesso anonimo per** abilitare l'accesso anonimo e fare clic su **OK.**
6.  Fare **clic su** Modifica in Comunicazioni **protette**.
7.  Deselezionare la casella di controllo Richiedi **canale sicuro (SSL).**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sul servizio SOAP COM+](com--soap-service-overview.md)
</dt> </dl>

 

 



