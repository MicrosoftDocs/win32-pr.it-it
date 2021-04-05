---
description: Attenersi a queste linee guida durante la creazione di un modulo merge a 64 bit.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Uso di moduli unione a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757805"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="5c287-103">Uso di moduli unione a 64 bit</span><span class="sxs-lookup"><span data-stu-id="5c287-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="5c287-104">Un modulo merge a 64 bit ha una delle caratteristiche identificate in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5c287-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="5c287-105">Il modulo merge contiene almeno un componente compilato per i sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="5c287-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="5c287-106">Il modulo merge non contiene componenti a 64 bit, ma deve essere utilizzato solo con i pacchetti [Windows Installer a 64 bit](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="5c287-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="5c287-107">I moduli merge possono essere usati come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5c287-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="5c287-108">Un modulo merge a 64 bit può essere unito in un pacchetto di [Windows Installer a 64 bit](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="5c287-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="5c287-109">Le proprietà di [**Riepilogo del modello**](template-summary.md) nel modulo merge e nel pacchetto di Windows Installer devono essere impostate sullo stesso tipo di processore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="5c287-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="5c287-110">Un modulo merge x64 può essere Unito solo a pacchetti x64 e un modulo merge Intel64 può essere Unito solo in pacchetti Intel64.</span><span class="sxs-lookup"><span data-stu-id="5c287-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="5c287-111">Un modulo merge a 32 bit può essere unito in pacchetti Windows Installer a 32 bit o [64 bit](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="5c287-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="5c287-112">Un modulo merge a 64 bit può essere unito in un pacchetto a 64 bit in un sistema operativo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5c287-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="5c287-113">Quando si crea un modulo unione a 64 bit, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="5c287-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="5c287-114">Utilizzare la stessa procedura generale utilizzata per la creazione di moduli unione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5c287-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="5c287-115">Per informazioni, vedere [About merge modules](about-merge-modules.md) e [Authoring merge modules](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="5c287-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="5c287-116">È necessario impostare la proprietà di [**Riepilogo del modello**](template-summary.md) con il valore Intel64 se si esegue un sistema Intel64.</span><span class="sxs-lookup"><span data-stu-id="5c287-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="5c287-117">È necessario impostare la proprietà di **Riepilogo del modello** con il valore x64 se si esegue un sistema x64.</span><span class="sxs-lookup"><span data-stu-id="5c287-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="5c287-118">Per informazioni, vedere [riferimento al flusso di informazioni di riepilogo del modulo merge](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5c287-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="5c287-119">Quando per lo stesso componente esistono entrambi i moduli unione a 32 bit e a 64 bit, è consigliabile che i moduli dispongano di firme diverse.</span><span class="sxs-lookup"><span data-stu-id="5c287-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="5c287-120">Questo consentirà a un pacchetto di contenere entrambe le versioni del componente.</span><span class="sxs-lookup"><span data-stu-id="5c287-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="5c287-121">Per ulteriori informazioni, vedere [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="5c287-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



