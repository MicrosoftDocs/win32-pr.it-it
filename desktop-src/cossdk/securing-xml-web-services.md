---
description: L'accesso alle applicazioni COM+ esposte come servizi Web XML è controllato dal server Web IIS, che elabora le richieste in ingresso.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Protezione dei servizi Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546964"
---
# <a name="securing-xml-web-services"></a>Protezione dei servizi Web XML

L'accesso alle applicazioni COM+ esposte come servizi Web XML è controllato dal server Web IIS, che elabora le richieste in ingresso. È anche possibile configurare IIS in modo da richiedere che le comunicazioni con il chiamante si s svolgono su un canale sicuro stabilito tramite il protocollo Secure Sockets Layer (SSL).

> [!Note]  
> Un servizio Web XML protetto non supporta l'accesso WKO tramite WSDL. I client che hanno installato il .NET Framework versione 1.1 possono invece chiamarlo in modalità CAO. Se i client di terze parti devono accedere al servizio Web XML tramite WSDL, è necessario consentire l'accesso anonimo.

 

> [!Note]  
> Per usare il protocollo SSL per stabilire un canale di comunicazione sicuro, è necessario ottenere e installare un certificato SSL.

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per selezionare il meccanismo di autenticazione per un servizio Web XML, seguire questa procedura:

1.  Fare clic con il pulsante **destro del Computer locale** sul desktop e scegliere **Gestisci.**

2.  In **Servizi e applicazioni** e Internet Information **Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML. Fare clic con il pulsante destro del mouse sull'icona della directory e **scegliere Proprietà.**

3.  Nella scheda **Sicurezza directory della** finestra di dialogo delle proprietà individuare Autenticazione e controllo di **accesso** e fare clic sul pulsante **Modifica** corrispondente.

4.  Nella finestra **di dialogo Metodi** di autenticazione in **Accesso** autenticato usare le caselle di controllo per selezionare i meccanismi di autenticazione da consentire. Fare clic su **OK**.

    > [!Note]  
    > È possibile configurare IIS per autenticare i chiamanti usando una delle opzioni seguenti nella finestra di dialogo Metodi di autenticazione **IIS:** Autenticazione **integrata Windows**, Autenticazione digest per i server di dominio Windows , Autenticazione di base (la password viene inviata **in** testo non **crittografato)** o Autenticazione **Passport .NET**. È anche possibile consentire l'accesso anonimo.

     

5.  Nella finestra di dialogo delle proprietà fare clic **su OK.**

Per consentire l'accesso anonimo non sicuro a un servizio Web XML, seguire questa procedura:

1.  Fare clic con il pulsante **destro del Computer locale** sul desktop e scegliere **Gestisci.**

2.  In **Servizi e applicazioni** e Internet Information **Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML. Fare clic con il pulsante destro del mouse sull'icona della directory e **scegliere Proprietà.**

3.  Nella scheda **Sicurezza directory della** finestra di dialogo delle proprietà individuare Autenticazione e controllo di **accesso** e fare clic sul pulsante **Modifica** corrispondente. Selezionare la casella **di controllo Abilita accesso** anonimo . Fare clic su **OK**.

4.  Nella scheda **Sicurezza directory della** finestra di dialogo delle proprietà individuare Comunicazioni **protette** e fare clic sul pulsante **Modifica** corrispondente. Deselezionare la **casella di controllo Richiedi canale sicuro (SSL).** Fare clic su **OK**.

5.  Nella finestra di dialogo delle proprietà fare clic **su OK.**

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="additional-security-considerations"></a>Considerazioni aggiuntive sulla sicurezza

Richiedendo un canale sicuro, è possibile proteggere la riservatezza dei dati s scambiati crittografando le comunicazioni tra il client e il servizio Web XML. Se si consente l'autenticazione tramite password non crittografate, è necessario un canale sicuro per evitare di esporre le password in rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Considerazioni sulla sicurezza dei servizi SOAP COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 



