---
description: Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente da attivazioni.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configurazione di un'applicazione server COM+ come applicazione di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877497"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="35f1f-103">Configurazione di un'applicazione server COM+ come applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="35f1f-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="35f1f-104">Un'applicazione server COM+ può essere creata come servizio per l'avvio automatico durante l'avvio del sistema o manualmente da attivazioni.</span><span class="sxs-lookup"><span data-stu-id="35f1f-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="35f1f-105">Se il servizio non viene avviato, l'opzione per la gestione degli errori specifica la gravità dell'errore e determina l'azione da intraprendere.</span><span class="sxs-lookup"><span data-stu-id="35f1f-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="35f1f-106">È inoltre disponibile l'opzione per configurare un servizio da eseguire come account di sistema locale, nonché l'opzione per l'assegnazione di un account utente specifico per il quale verrà eseguita l'applicazione server COM+.</span><span class="sxs-lookup"><span data-stu-id="35f1f-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="35f1f-107">Le dipendenze possono essere selezionate anche da un elenco di servizi registrati nel computer utilizzando Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="35f1f-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="35f1f-108">In questo modo verranno determinati i servizi che devono essere eseguiti prima dell'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="35f1f-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="35f1f-109">**Per configurare un'applicazione COM+ per l'esecuzione come servizio**</span><span class="sxs-lookup"><span data-stu-id="35f1f-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="35f1f-110">Nell'albero della console dello strumento di amministrazione Servizi componenti individuare l'applicazione server COM+ che si desidera eseguire come servizio.</span><span class="sxs-lookup"><span data-stu-id="35f1f-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="35f1f-111">Fare clic con il pulsante destro del mouse sull'applicazione server COM+, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="35f1f-112">Nella finestra di dialogo **Proprietà** fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="35f1f-113">Nella casella **tipo di attivazione** selezionare la casella di controllo **Esegui applicazione come servizio NT** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="35f1f-114">La casella di controllo **Esegui applicazione come servizio NT** è abilitata solo per le applicazioni server ed è disabilitata per le applicazioni di libreria.</span><span class="sxs-lookup"><span data-stu-id="35f1f-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="35f1f-115">Fare clic sul pulsante **Imposta nuovo servizio** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="35f1f-116">Nella casella **tipo di avvio** nella finestra di dialogo **nome servizio** selezionare **automatico** o **manuale**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="35f1f-117">Opzionale Per specificare l'azione da intraprendere per un particolare errore, selezionare **Ignora**, **normale**, **grave** o **critico** nella casella **Gestione errori** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="35f1f-118">Il comportamento associato a ogni opzione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="35f1f-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="35f1f-119">**Ignore**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-119">**Ignore**.</span></span> <span data-ttu-id="35f1f-120">Il programma di avvio registra l'errore ma continua l'operazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="35f1f-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="35f1f-121">**Normale**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-121">**Normal**.</span></span> <span data-ttu-id="35f1f-122">L'errore viene registrato, viene visualizzata una finestra di messaggio e il programma di avvio continua l'operazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="35f1f-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="35f1f-123">**Grave**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-123">**Severe**.</span></span> <span data-ttu-id="35f1f-124">L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione corretta nota.</span><span class="sxs-lookup"><span data-stu-id="35f1f-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="35f1f-125">Se è l'ultima configurazione ben nota che viene avviata quando viene registrato l'errore, l'operazione di avvio continua.</span><span class="sxs-lookup"><span data-stu-id="35f1f-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="35f1f-126">**Critica**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-126">**Critical**.</span></span> <span data-ttu-id="35f1f-127">L'errore viene registrato e il sistema viene riavviato con l'ultima configurazione corretta nota.</span><span class="sxs-lookup"><span data-stu-id="35f1f-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="35f1f-128">Se è l'ultima configurazione corretta nota che viene avviata quando viene registrato l'errore, l'operazione di avvio non riesce.</span><span class="sxs-lookup"><span data-stu-id="35f1f-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="35f1f-129">Opzionale Per impostare altri servizi come dipendenti, selezionare i servizi dipendenti dall'elenco nella casella **dipendenze** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="35f1f-130">Opzionale Per indicare che il servizio deve essere autorizzato a interagire con il desktop, selezionare la casella **di controllo Consenti al servizio di interagire con il desktop** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="35f1f-131">Fare clic su **Crea**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-131">Click **Create**.</span></span>

11. <span data-ttu-id="35f1f-132">Opzionale Per assegnare il servizio a un account utente:</span><span class="sxs-lookup"><span data-stu-id="35f1f-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="35f1f-133">Nella scheda **identità** selezionare **questo utente**.</span><span class="sxs-lookup"><span data-stu-id="35f1f-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="35f1f-134">Per selezionare l'utente, immettere il nome utente nella casella **utente** oppure fare clic sul pulsante **Sfoglia** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="35f1f-135">Immettere la password per l'account utente nella casella **password** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="35f1f-136">Immettere la stessa password nella casella **Conferma password** .</span><span class="sxs-lookup"><span data-stu-id="35f1f-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



