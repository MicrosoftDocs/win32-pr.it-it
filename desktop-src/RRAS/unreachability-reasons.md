---
title: Motivi di non raggiungibilità
description: Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047094"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="27c7e-103">Motivi di non raggiungibilità</span><span class="sxs-lookup"><span data-stu-id="27c7e-103">Unreachability Reasons</span></span>

<span data-ttu-id="27c7e-104">Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="27c7e-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="27c7e-105">Valore</span><span class="sxs-lookup"><span data-stu-id="27c7e-105">Value</span></span>                                       | <span data-ttu-id="27c7e-106">Significato</span><span class="sxs-lookup"><span data-stu-id="27c7e-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c7e-107">\_amministratore interfaccia \_ MPR \_ disabilitato</span><span class="sxs-lookup"><span data-stu-id="27c7e-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="27c7e-108">L'amministratore ha disabilitato l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c7e-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="27c7e-109">\_errore di \_ connessione dell'interfaccia MPR \_</span><span class="sxs-lookup"><span data-stu-id="27c7e-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="27c7e-110">Il tentativo di connessione precedente non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="27c7e-110">The previous connection attempt failed.</span></span> <span data-ttu-id="27c7e-111">Esaminare il membro **dwLastError** per il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="27c7e-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="27c7e-112">\_ \_ restrizione delle ore di connessione dell'interfaccia MPR \_ \_</span><span class="sxs-lookup"><span data-stu-id="27c7e-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="27c7e-113">La connessione remota non è consentita all'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="27c7e-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="27c7e-114">\_interfaccia MPR \_ \_ di \_ risorse insufficienti</span><span class="sxs-lookup"><span data-stu-id="27c7e-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="27c7e-115">Non sono disponibili porte o dispositivi da usare.</span><span class="sxs-lookup"><span data-stu-id="27c7e-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="27c7e-116">\_servizio di interfaccia MPR \_ \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="27c7e-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="27c7e-117">Il servizio è in pausa.</span><span class="sxs-lookup"><span data-stu-id="27c7e-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="27c7e-118">\_interfaccia MPR \_ senza \_ media \_ Sense</span><span class="sxs-lookup"><span data-stu-id="27c7e-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="27c7e-119">Il cavo di rete è disconnesso dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="27c7e-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="27c7e-120">\_interfaccia MPR \_ senza \_ dispositivo</span><span class="sxs-lookup"><span data-stu-id="27c7e-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="27c7e-121">La scheda di rete è stata rimossa dal computer.</span><span class="sxs-lookup"><span data-stu-id="27c7e-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="27c7e-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27c7e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c7e-123">**\_Interfaccia MPR \_ 0**</span><span class="sxs-lookup"><span data-stu-id="27c7e-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="27c7e-124">**\_Interfaccia MPR \_ 1**</span><span class="sxs-lookup"><span data-stu-id="27c7e-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="27c7e-125">**\_IFROW MIB**</span><span class="sxs-lookup"><span data-stu-id="27c7e-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="27c7e-126">**\_IFSTATUS MIB**</span><span class="sxs-lookup"><span data-stu-id="27c7e-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 