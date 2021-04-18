---
description: L'accesso alle applicazioni COM+ esposte come servizi Web XML è controllato dal server Web IIS, che elabora le richieste in ingresso.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Protezione dei servizi Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305208"
---
# <a name="securing-xml-web-services"></a>Protezione dei servizi Web XML

L'accesso alle applicazioni COM+ esposte come servizi Web XML è controllato dal server Web IIS, che elabora le richieste in ingresso. È inoltre possibile configurare IIS in modo da richiedere che le comunicazioni con il chiamante avvengano su un canale protetto stabilito utilizzando il protocollo Secure Sockets Layer (SSL).

> [!Note]  
> Un servizio Web XML protetto non supporta l'accesso WKO tramite WSDL. I client che hanno installato la versione di .NET Framework 1,1 possono invece chiamarlo in modalità CAO. Se i client di terze parti devono accedere al servizio Web XML tramite WSDL, è necessario consentire l'accesso anonimo.

 

> [!Note]  
> Per utilizzare il protocollo SSL per stabilire un canale di comunicazione protetto, è necessario ottenere e installare un certificato SSL.

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per selezionare il meccanismo di autenticazione per un servizio Web XML, attenersi alla procedura seguente:

1.  Fare clic con il pulsante destro del mouse sull'icona **computer locale** sul desktop e scegliere **Gestisci**.

2.  In **Servizi e applicazioni** e **Internet Information Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML. Fare clic con il pulsante destro del mouse sull'icona della directory e scegliere **Proprietà**.

3.  Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **autenticazione e controllo di accesso** e fare clic sul pulsante **modifica** corrispondente.

4.  Nella finestra di dialogo **metodi di autenticazione** , in **accesso con autenticazione**, utilizzare le caselle di controllo per selezionare i meccanismi di autenticazione che si desidera consentire. Fare clic su **OK**.

    > [!Note]  
    > È possibile configurare IIS per l'autenticazione dei chiamanti utilizzando una delle opzioni seguenti nella finestra di dialogo **metodi di autenticazione** IIS: **autenticazione integrata di Windows**, **autenticazione del digest per server di dominio Windows**, **autenticazione di base (la password viene inviata in testo non crittografato)** o **autenticazione .NET Passport**. È anche possibile consentire l'accesso anonimo.

     

5.  Nella finestra di dialogo Proprietà fare clic su **OK**.

Per consentire l'accesso anonimo non sicuro a un servizio Web XML, attenersi alla procedura seguente:

1.  Fare clic con il pulsante destro del mouse sull'icona **computer locale** sul desktop e scegliere **Gestisci**.

2.  In **Servizi e applicazioni** e **Internet Information Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML. Fare clic con il pulsante destro del mouse sull'icona della directory e scegliere **Proprietà**.

3.  Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **autenticazione e controllo di accesso** e fare clic sul pulsante **modifica** corrispondente. Selezionare la casella di controllo **Abilita accesso anonimo** . Fare clic su **OK**.

4.  Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **comunicazioni sicure** e fare clic sul pulsante **modifica** corrispondente. Deselezionare la casella di controllo **Richiedi canale sicuro (SSL)** . Fare clic su **OK**.

5.  Nella finestra di dialogo Proprietà fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="additional-security-considerations"></a>Considerazioni aggiuntive sulla sicurezza

Richiedendo un canale sicuro, si protegge la riservatezza dei dati scambiati crittografando le comunicazioni tra il client e il servizio Web XML. Se si consente l'autenticazione tramite password con testo non crittografato, è necessario disporre di un canale sicuro per evitare l'esposizione delle password sulla rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Considerazioni sulla sicurezza del servizio SOAP COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 



