---
description: Un'interfaccia smart card è costituita da un set predefinito di servizi disponibili all'interno di una smart card, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfacce smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758390"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="fa851-103">Interfacce smart card</span><span class="sxs-lookup"><span data-stu-id="fa851-103">Smart Card Interfaces</span></span>

<span data-ttu-id="fa851-104">Un'interfaccia [*Smart Card*](../secgloss/s-gly.md) è costituita da un set predefinito di servizi disponibili all'interno di una *Smart Card*, dai protocolli necessari per richiamare i servizi e da eventuali presupposti relativi al contesto dei servizi.</span><span class="sxs-lookup"><span data-stu-id="fa851-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="fa851-105">Per quanto riguarda le smart card, il termine "Interface" è simile a quello usato in COM, che a sua volta è un concetto simile all'identificatore dell'applicazione ISO 7816/5 ma con un ambito diverso.</span><span class="sxs-lookup"><span data-stu-id="fa851-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="fa851-106">Ogni interfaccia smart card è identificata da un GUID.</span><span class="sxs-lookup"><span data-stu-id="fa851-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="fa851-107">Ad esempio, è possibile definire un'interfaccia che fornisce informazioni Biorhythm al suo titolare.</span><span class="sxs-lookup"><span data-stu-id="fa851-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="fa851-108">Se una determinata smart card supporta questo servizio, potrebbe richiedere di supportare il GUID dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fa851-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="fa851-109">Usando i GUID di interfaccia, un'applicazione può cercare un particolare set di interfacce, individuando qualsiasi scheda che supporta tale set, per completare un'attività.</span><span class="sxs-lookup"><span data-stu-id="fa851-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="fa851-110">Sebbene un'interfaccia disponga di un solo GUID, può essere implementata in modo diverso in schede diverse.</span><span class="sxs-lookup"><span data-stu-id="fa851-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="fa851-111">Ad esempio, l'interfaccia Biorhythm menzionata in precedenza può includere diverse implementazioni, ma viene fatto riferimento a tutti con lo stesso GUID.</span><span class="sxs-lookup"><span data-stu-id="fa851-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="fa851-112">Le diverse implementazioni non modificano l'interazione tra l'applicazione e la smart card; Tuttavia, l'interazione tra il [*provider di servizi*](../secgloss/c-gly.md) e le smart card può variare in base all'implementazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fa851-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="fa851-113">Il set di interfacce supportato da una smart card viene definito durante l'introduzione della smart card (vedere [introduzione di smart card al sistema](introducing-smart-cards-to-the-system.md)).</span><span class="sxs-lookup"><span data-stu-id="fa851-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
