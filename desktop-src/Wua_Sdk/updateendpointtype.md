---
description: Definisce il tipo di endpoint che possono essere utilizzati per connettersi a un servizio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumerazione UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525074"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="eefdd-103">Enumerazione UpdateEndpointType</span><span class="sxs-lookup"><span data-stu-id="eefdd-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="eefdd-104">Definisce il tipo di endpoint che possono essere utilizzati per connettersi a un servizio.</span><span class="sxs-lookup"><span data-stu-id="eefdd-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefdd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eefdd-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="eefdd-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="eefdd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eefdd-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="eefdd-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-108">Un endpoint client-server usato per connettersi al servizio di aggiornamento, ad esempio Windows Update, Microsoft Update e server WSUS in un ambiente aziendale, per trovare informazioni sugli aggiornamenti che potrebbero essere applicabili al computer.</span><span class="sxs-lookup"><span data-stu-id="eefdd-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="eefdd-109">Il servizio di aggiornamento restituisce informazioni sugli aggiornamenti che sono stati pubblicati, modificati o ritirati a partire dall'ultima volta in cui il client ha eseguito una sincronizzazione con il server.</span><span class="sxs-lookup"><span data-stu-id="eefdd-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="eefdd-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-111">Un endpoint di Reporting utilizzato quando il client segnala i risultati di analisi, download e installazioni di nuovo nel servizio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="eefdd-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="eefdd-112">Nel caso di servizi pubblici (Windows Update e Microsoft Update), questa operazione viene eseguita per finalità di monitoraggio della qualità.</span><span class="sxs-lookup"><span data-stu-id="eefdd-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="eefdd-113">Nel caso di servizi privati, ad esempio un server WSUS aziendale, il tipo di endpoint Thhis consente anche al server di raccogliere l'inventario e altre informazioni sui computer client gestiti.</span><span class="sxs-lookup"><span data-stu-id="eefdd-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="eefdd-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-115">Un endpoint di aggiornamento automatico utilizzato quando il computer client contatta un servizio di aggiornamento per verificare se è presente una nuova versione del software client agente Windows Update.</span><span class="sxs-lookup"><span data-stu-id="eefdd-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="eefdd-116">L'endpoint di aggiornamento automatico usa un protocollo diverso, quindi l'endpoint Client-Server in modo che gli aggiornamenti automatici possano essere distribuiti anche se si verifica una condizione di errore che potrebbe impedire la normale sincronizzazione del client-server di lavorare su un computer client specifico.</span><span class="sxs-lookup"><span data-stu-id="eefdd-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="eefdd-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-118">Un endpoint del regolamento utilizzato quando il computer client contatta il servizio di regolamentazione per agire su un particolare aggiornamento applicabile al computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eefdd-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="eefdd-119">Il servizio del regolamento può indicare se l'aggiornamento è "regolato" (anche noto come "limitato"). in altre parole, il servizio di regolamentazione può indicare al computer client che non deve agire su un particolare aggiornamento, anche se tale aggiornamento sembra essere applicabile.</span><span class="sxs-lookup"><span data-stu-id="eefdd-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="eefdd-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-121">Un endpoint di destinazione semplice utilizzato solo con servizi privati (server WSUS negli ambienti aziendali).</span><span class="sxs-lookup"><span data-stu-id="eefdd-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="eefdd-122">In un ambiente aziendale, i computer client possono essere assegnati a determinati gruppi di destinazione e gli aggiornamenti possono essere approvati per l'installazione in computer in alcuni gruppi, ma non altri.</span><span class="sxs-lookup"><span data-stu-id="eefdd-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="eefdd-123">Ad esempio, l'amministratore di WSUS può creare un gruppo di "test" per i computer utilizzati per testare nuovi aggiornamenti e l'amministratore può approvare gli aggiornamenti appena rilasciati per l'installazione nei computer del gruppo di test senza approvarli per l'installazione in altri computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="eefdd-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="eefdd-124">Lo scambio di destinazione semplice viene utilizzato per consentire a un computer client di registrarsi con il server WSUS e per consentire al server di indicare al computer client il gruppo in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="eefdd-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span><span class="sxs-lookup"><span data-stu-id="eefdd-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-126">Un endpoint client-server protetto che consente a un client di ottenere informazioni sulle app che richiedono licenze, in modo che possano essere usate in un computer client.</span><span class="sxs-lookup"><span data-stu-id="eefdd-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="eefdd-127">Questo framework di licenze è attualmente utilizzato solo da Windows 8 per distribuire le app e gli aggiornamenti ottenuti tramite Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eefdd-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="eefdd-128">L'endpoint client-server protetto non è attualmente utilizzato da Windows Update, Microsoft Update o WSUS.</span><span class="sxs-lookup"><span data-stu-id="eefdd-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="eefdd-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span><span class="sxs-lookup"><span data-stu-id="eefdd-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="eefdd-130">L'endpoint di autenticazione del servizio secondario viene usato da un client per fornire l'autenticazione prima di ottenere informazioni sulle app che richiedono licenze, in modo che possano essere usate in un computer client.</span><span class="sxs-lookup"><span data-stu-id="eefdd-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="eefdd-131">Questo framework di licenze è attualmente utilizzato solo da Windows 8 per distribuire le app e gli aggiornamenti ottenuti tramite Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eefdd-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="eefdd-132">L'endpoint di autenticazione del servizio secondario non è attualmente utilizzato da Windows Update, Microsoft Update o WSUS.</span><span class="sxs-lookup"><span data-stu-id="eefdd-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eefdd-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eefdd-133">Requirements</span></span>



| <span data-ttu-id="eefdd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="eefdd-134">Requirement</span></span> | <span data-ttu-id="eefdd-135">Valore</span><span class="sxs-lookup"><span data-stu-id="eefdd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefdd-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eefdd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eefdd-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eefdd-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="eefdd-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eefdd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eefdd-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eefdd-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eefdd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eefdd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eefdd-141"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="eefdd-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="eefdd-142">IDL</span><span class="sxs-lookup"><span data-stu-id="eefdd-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eefdd-143"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eefdd-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




