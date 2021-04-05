---
title: API del provider Remote Desktop Protocol
description: Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955059"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="12564-103">API del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="12564-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="12564-104">Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.</span><span class="sxs-lookup"><span data-stu-id="12564-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="12564-105">Quando si carica Windows Server, viene avviato il servizio di Servizi Desktop remoto (noto anche come gestione connessione remota (RCM)).</span><span class="sxs-lookup"><span data-stu-id="12564-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="12564-106">Il servizio avvia anche gli oggetti listener per i provider di Remote Desktop Protocol che a loro volta restano in ascolto delle connessioni client.</span><span class="sxs-lookup"><span data-stu-id="12564-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="12564-107">Il servizio e i provider di protocollo sono oggetti in modalità utente che comunicano usando le API descritte in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="12564-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="12564-108">I provider di protocollo possono comunicare con i driver in modalità kernel utilizzando i controlli di input/output (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="12564-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="12564-109">Questo aspetto è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="12564-109">This is shown in the following illustration.</span></span>

![architettura API del protocollo personalizzato](images/protocol-architecture.png)

<span data-ttu-id="12564-111">Microsoft ha implementato il Remote Desktop Protocol (RDP) per fornire la comunicazione tra il servizio di Servizi Desktop remoto e le connessioni client.</span><span class="sxs-lookup"><span data-stu-id="12564-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="12564-112">È possibile creare un protocollo personalizzato utilizzando interfacce, strutture, unioni e tipi di enumerazione che costituiscono l'API del provider Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="12564-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="12564-113">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="12564-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="12564-114">Creazione di un provider di Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="12564-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="12564-115">Informazioni sulla creazione di un provider di Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="12564-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="12564-116">Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="12564-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="12564-117">Riferimento al provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="12564-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="12564-118">Contiene interfacce, strutture, unioni e tipi di enumerazione che consentono di creare un Remote Desktop Protocol personalizzato (RDP).</span><span class="sxs-lookup"><span data-stu-id="12564-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="12564-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12564-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12564-120">Informazioni su Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="12564-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




