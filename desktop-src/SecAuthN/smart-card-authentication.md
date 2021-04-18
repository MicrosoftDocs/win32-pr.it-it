---
description: Autenticazione con smart card
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticazione con smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316230"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="76c82-103">Autenticazione con smart card</span><span class="sxs-lookup"><span data-stu-id="76c82-103">Smart Card Authentication</span></span>

<span data-ttu-id="76c82-104">Le parti di base del [*sottosistema Smart Card*](../secgloss/s-gly.md) sono basate sugli standard PC/SC (vedere le specifiche in [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="76c82-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="76c82-105">Queste parti di base includono:</span><span class="sxs-lookup"><span data-stu-id="76c82-105">These basic parts include:</span></span>

-   <span data-ttu-id="76c82-106">[*Gestore di risorse*](../secgloss/r-gly.md) che usa un'API Windows.</span><span class="sxs-lookup"><span data-stu-id="76c82-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="76c82-107">[*Interfaccia utente*](../secgloss/u-gly.md) (UI) che funziona con gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="76c82-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="76c82-108">Diversi [*provider di servizi*](../secgloss/s-gly.md) di base che forniscono accesso a servizi specifici.</span><span class="sxs-lookup"><span data-stu-id="76c82-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="76c82-109">Diversamente dall'API Windows di Resource Manager, i provider di servizi usano un modello di interfaccia COM per fornire servizi [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="76c82-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="76c82-110">Nella figura seguente sono illustrate le relazioni di queste parti nell'architettura complessiva delle smart card.</span><span class="sxs-lookup"><span data-stu-id="76c82-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![architettura Smart Card](images/smartovr2a.png)

<span data-ttu-id="76c82-112">Per informazioni sul funzionamento del [*sottosistema Smart Card*](../secgloss/s-gly.md) con altri servizi disponibili in Microsoft Internet Security Framework, vedere [relazioni con altri servizi](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="76c82-113">Per informazioni sull'autenticazione con smart card, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="76c82-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="76c82-114">Argomenti</span><span class="sxs-lookup"><span data-stu-id="76c82-114">Topics</span></span>                                                                      | <span data-ttu-id="76c82-115">Contenuto</span><span class="sxs-lookup"><span data-stu-id="76c82-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76c82-116">Concetti relativi alle smart card</span><span class="sxs-lookup"><span data-stu-id="76c82-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="76c82-117">Concetti di base e Descrizione dell'interazione tra utenti e smart card.</span><span class="sxs-lookup"><span data-stu-id="76c82-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="76c82-118">Gestione risorse smart card</span><span class="sxs-lookup"><span data-stu-id="76c82-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="76c82-119">Informazioni sull'API di Resource Manager, che consente di gestire l'accesso ai [*lettori*](../secgloss/r-gly.md) e alle [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="76c82-120">Interfaccia utente della smart card</span><span class="sxs-lookup"><span data-stu-id="76c82-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="76c82-121">Informazioni sulla finestra di [*dialogo comune della smart card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="76c82-122">Provider di servizi Smart Card</span><span class="sxs-lookup"><span data-stu-id="76c82-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="76c82-123">Informazioni su interfacce, comandi e wrapper che forniscono funzionalità per smart card.</span><span class="sxs-lookup"><span data-stu-id="76c82-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="76c82-124">Inoltre, è possibile trovare gli attuali sviluppi delle smart card Microsoft all'indirizzo [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="76c82-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
