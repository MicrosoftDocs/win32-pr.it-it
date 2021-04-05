---
description: Se uno o più dei seguenti casi sono veri, i provider di componenti condivisi dovrebbero considerare la possibilità di rendere disponibile il componente come assembly side-by-side.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: È necessario fornire un componente condiviso come assembly affiancato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884526"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="bc6bc-103">È necessario fornire un componente condiviso come assembly affiancato?</span><span class="sxs-lookup"><span data-stu-id="bc6bc-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="bc6bc-104">Per i provider di componenti condivisi è consigliabile rendere disponibile il componente come assembly affiancato se si verificano una o più delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc6bc-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="bc6bc-105">Il componente espone un Application Programming Interface completo utilizzato da molte applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="bc6bc-106">Ad esempio, un componente come MSHTML, che consente alle applicazioni C e C++ di accedere al modello a oggetti DHTML (Dynamic HTML).</span><span class="sxs-lookup"><span data-stu-id="bc6bc-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="bc6bc-107">Il componente è già condiviso da più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="bc6bc-108">Ad esempio, un componente come COMCTL32, che consente alle applicazioni di accedere ai controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="bc6bc-109">Il componente è un nuovo componente.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-109">The component is a new component.</span></span>
-   <span data-ttu-id="bc6bc-110">Il componente è un componente in modalità utente e non un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="bc6bc-111">Non tutti i componenti sono un candidato adatto per un assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="bc6bc-112">Un componente non è un candidato adatto per un assembly affiancato se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc6bc-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="bc6bc-113">Il componente gestisce la comunicazione tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-113">The component handles communication between applications.</span></span> <span data-ttu-id="bc6bc-114">Ad esempio, parti di OLE32 non rendono un assembly side-by-side efficace perché non si vogliono avere due versioni diverse delle parti che coordinano la comunicazione tra le applicazioni eseguite nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="bc6bc-115">Il componente gestisce un dispositivo fisico o virtuale per il sistema.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="bc6bc-116">Ad esempio un driver di dispositivo per uno spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="bc6bc-117">In alcuni casi potrebbe essere possibile per lo sviluppatore del componente riprogettare un componente esistente per renderlo idoneo per la pubblicazione come assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="bc6bc-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="bc6bc-118">Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="bc6bc-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



