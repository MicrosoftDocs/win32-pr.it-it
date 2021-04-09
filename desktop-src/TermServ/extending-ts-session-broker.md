---
title: Estensione di broker di sessione di Servizi terminal
description: È possibile estendere TS \ 160; Broker di sessione mediante l'interfaccia COM IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729290"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="77cec-103">Estensione di broker di sessione di Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="77cec-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="77cec-104">Gestore sessioni Servizi terminal determina se un utente che avvia una connessione dispone già di una sessione aperta.</span><span class="sxs-lookup"><span data-stu-id="77cec-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="77cec-105">In tal caso, broker di sessione di Servizi terminal instrada la connessione in ingresso al server host sessione Desktop remoto (host sessione Desktop remoto) con la sessione esistente.</span><span class="sxs-lookup"><span data-stu-id="77cec-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="77cec-106">In caso contrario, broker di sessione di Servizi terminal instrada la connessione in ingresso al server Host sessione Desktop remoto con il minor numero di sessioni.</span><span class="sxs-lookup"><span data-stu-id="77cec-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="77cec-107">È possibile estendere broker di sessione di Servizi terminal tramite l'interfaccia com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="77cec-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="77cec-108">È possibile utilizzare questa interfaccia per gestire le connessioni ai server Host sessione Desktop remoto e a qualsiasi tipo di connessione di Remote Desktop Protocol (RDP), ad esempio, le connessioni alle macchine virtuali guest che eseguono Windows Vista Enterprise centralizzate desktop (VECD) in un host macchina virtuale Hyper-V di Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="77cec-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="77cec-109">L'interfaccia [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) offre diversi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="77cec-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="77cec-110">Non è necessario installare un agente nel client o nel server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="77cec-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="77cec-111">Il plug-in può interagire senza interruzioni con altri servizi ruolo Servizi Desktop remoto, ad esempio Desktop remoto Gateway (Gateway Desktop remoto) e basarsi sulle informazioni provenienti da broker di sessione di Servizi terminal sugli stati di sessione e computer.</span><span class="sxs-lookup"><span data-stu-id="77cec-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="77cec-112">È possibile usare il plug-in per gestire le connessioni con i dispositivi client o server che supportano RDP 5,2 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="77cec-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="77cec-113">È possibile utilizzare il plug-in per abilitare le soluzioni desktop centralizzate di Windows Vista Enterprise.</span><span class="sxs-lookup"><span data-stu-id="77cec-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="77cec-114">Quando si implementano i metodi di questa interfaccia, tenere presenti i seguenti aspetti:</span><span class="sxs-lookup"><span data-stu-id="77cec-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="77cec-115">Broker di sessione di Servizi terminal può chiamare i metodi di questo oggetto COM da più thread.</span><span class="sxs-lookup"><span data-stu-id="77cec-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="77cec-116">Se uno dei metodi chiamati non viene restituito immediatamente e correttamente, broker di sessione di Servizi terminal non effettua più chiamate al plug-in e ripristina la logica di bilanciamento del carico nativa.</span><span class="sxs-lookup"><span data-stu-id="77cec-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="77cec-117">Per riprendere le chiamate al plug-in, è necessario riavviare il servizio Gestore sessioni Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="77cec-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="77cec-118">È necessario registrare il plug-in come oggetto COM a livello di sistema utilizzando Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="77cec-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="77cec-119">Poiché il servizio Gestore sessioni Servizi terminal viene eseguito con l'account "NetworkService", è necessario assegnare all'account "NetworkService" le autorizzazioni di avvio, attivazione e accesso richieste usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="77cec-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="77cec-120">Il servizio Gestore sessioni Servizi terminal Cerca il CLSID dell'oggetto COM che rappresenta il plug-in nella seguente sottochiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="77cec-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="77cec-121">**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **Tssdis** \\ **parametri** \\ **ExtensibilityPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="77cec-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="77cec-122">Per ulteriori informazioni su Dcomcnfg.exe, vedere [Abilitazione della sicurezza com tramite DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="77cec-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77cec-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77cec-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77cec-124">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="77cec-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 