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
# <a name="securing-xml-web-services"></a><span data-ttu-id="e39ff-103">Protezione dei servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="e39ff-103">Securing XML Web Services</span></span>

<span data-ttu-id="e39ff-104">L'accesso alle applicazioni COM+ esposte come servizi Web XML è controllato dal server Web IIS, che elabora le richieste in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e39ff-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="e39ff-105">È inoltre possibile configurare IIS in modo da richiedere che le comunicazioni con il chiamante avvengano su un canale protetto stabilito utilizzando il protocollo Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="e39ff-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="e39ff-106">Un servizio Web XML protetto non supporta l'accesso WKO tramite WSDL.</span><span class="sxs-lookup"><span data-stu-id="e39ff-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="e39ff-107">I client che hanno installato la versione di .NET Framework 1,1 possono invece chiamarlo in modalità CAO.</span><span class="sxs-lookup"><span data-stu-id="e39ff-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="e39ff-108">Se i client di terze parti devono accedere al servizio Web XML tramite WSDL, è necessario consentire l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="e39ff-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="e39ff-109">Per utilizzare il protocollo SSL per stabilire un canale di comunicazione protetto, è necessario ottenere e installare un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="e39ff-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="e39ff-110">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="e39ff-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="e39ff-111">Per selezionare il meccanismo di autenticazione per un servizio Web XML, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="e39ff-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="e39ff-112">Fare clic con il pulsante destro del mouse sull'icona **computer locale** sul desktop e scegliere **Gestisci**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="e39ff-113">In **Servizi e applicazioni** e **Internet Information Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="e39ff-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="e39ff-114">Fare clic con il pulsante destro del mouse sull'icona della directory e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="e39ff-115">Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **autenticazione e controllo di accesso** e fare clic sul pulsante **modifica** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e39ff-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="e39ff-116">Nella finestra di dialogo **metodi di autenticazione** , in **accesso con autenticazione**, utilizzare le caselle di controllo per selezionare i meccanismi di autenticazione che si desidera consentire.</span><span class="sxs-lookup"><span data-stu-id="e39ff-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="e39ff-117">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="e39ff-118">È possibile configurare IIS per l'autenticazione dei chiamanti utilizzando una delle opzioni seguenti nella finestra di dialogo **metodi di autenticazione** IIS: **autenticazione integrata di Windows**, **autenticazione del digest per server di dominio Windows**, **autenticazione di base (la password viene inviata in testo non crittografato)** o **autenticazione .NET Passport**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="e39ff-119">È anche possibile consentire l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="e39ff-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="e39ff-120">Nella finestra di dialogo Proprietà fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="e39ff-121">Per consentire l'accesso anonimo non sicuro a un servizio Web XML, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="e39ff-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="e39ff-122">Fare clic con il pulsante destro del mouse sull'icona **computer locale** sul desktop e scegliere **Gestisci**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="e39ff-123">In **Servizi e applicazioni** e **Internet Information Service** individuare l'icona corrispondente alla directory radice virtuale per il servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="e39ff-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="e39ff-124">Fare clic con il pulsante destro del mouse sull'icona della directory e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="e39ff-125">Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **autenticazione e controllo di accesso** e fare clic sul pulsante **modifica** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e39ff-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="e39ff-126">Selezionare la casella di controllo **Abilita accesso anonimo** .</span><span class="sxs-lookup"><span data-stu-id="e39ff-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="e39ff-127">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-127">Click **OK**.</span></span>

4.  <span data-ttu-id="e39ff-128">Nella scheda **sicurezza directory** della finestra di dialogo Proprietà individuare **comunicazioni sicure** e fare clic sul pulsante **modifica** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e39ff-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="e39ff-129">Deselezionare la casella di controllo **Richiedi canale sicuro (SSL)** .</span><span class="sxs-lookup"><span data-stu-id="e39ff-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="e39ff-130">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-130">Click **OK**.</span></span>

5.  <span data-ttu-id="e39ff-131">Nella finestra di dialogo Proprietà fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e39ff-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="e39ff-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e39ff-132">Visual Basic</span></span>

<span data-ttu-id="e39ff-133">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="e39ff-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="e39ff-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="e39ff-134">C/C++</span></span>

<span data-ttu-id="e39ff-135">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="e39ff-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="e39ff-136">Considerazioni aggiuntive sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="e39ff-136">Additional Security Considerations</span></span>

<span data-ttu-id="e39ff-137">Richiedendo un canale sicuro, si protegge la riservatezza dei dati scambiati crittografando le comunicazioni tra il client e il servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="e39ff-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="e39ff-138">Se si consente l'autenticazione tramite password con testo non crittografato, è necessario disporre di un canale sicuro per evitare l'esposizione delle password sulla rete.</span><span class="sxs-lookup"><span data-stu-id="e39ff-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e39ff-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e39ff-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39ff-140">Accesso ai servizi Web XML in modalità CAO</span><span class="sxs-lookup"><span data-stu-id="e39ff-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="e39ff-141">Accesso ai servizi Web XML in modalità WKO</span><span class="sxs-lookup"><span data-stu-id="e39ff-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="e39ff-142">Considerazioni sulla sicurezza del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="e39ff-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="e39ff-143">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="e39ff-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 



