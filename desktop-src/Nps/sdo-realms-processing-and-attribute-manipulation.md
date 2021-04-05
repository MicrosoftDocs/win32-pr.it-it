---
title: Elaborazione degli ambiti e manipolazione degli attributi
description: L'elaborazione dell'area di autenticazione, nota anche come manipolazione degli attributi, fa riferimento a trasformare il nome dell'utente che richiede l'accesso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728567"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="9d55c-103">Elaborazione degli ambiti e manipolazione degli attributi</span><span class="sxs-lookup"><span data-stu-id="9d55c-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="9d55c-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9d55c-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="9d55c-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="9d55c-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="9d55c-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="9d55c-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="9d55c-107">L'elaborazione dell'area di autenticazione, nota anche come manipolazione degli attributi, fa riferimento a trasformare il nome dell'utente che richiede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9d55c-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="9d55c-108">È anche possibile modificare l'ID della stazione chiamante e l'ID della stazione chiamata.</span><span class="sxs-lookup"><span data-stu-id="9d55c-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="9d55c-109">Le regole di elaborazione dell'area di autenticazione fanno parte della raccolta di attributi del profilo proxy.</span><span class="sxs-lookup"><span data-stu-id="9d55c-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="9d55c-110">Per ogni manipolazione è necessario creare due attributi della [regola di manipolazione](/windows/desktop/Nps/sdo-manipulation-rule) .</span><span class="sxs-lookup"><span data-stu-id="9d55c-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="9d55c-111">Ognuno di questi attributi è un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="9d55c-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="9d55c-112">La prima regola contiene un'espressione regolare che rappresenta il criterio di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="9d55c-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="9d55c-113">La seconda regola contiene un'espressione regolare che rappresenta il testo di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="9d55c-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="9d55c-114">È anche necessario creare un attributo di [destinazione della manipolazione](/windows/desktop/Nps/sdo-manipulation-target) .</span><span class="sxs-lookup"><span data-stu-id="9d55c-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="9d55c-115">Questo attributo è un'enumerazione che specifica la parte delle informazioni dell'utente da modificare.</span><span class="sxs-lookup"><span data-stu-id="9d55c-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="9d55c-116">L'ordine in cui vengono creati gli attributi è importante.</span><span class="sxs-lookup"><span data-stu-id="9d55c-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="9d55c-117">NPS elabora gli attributi nell'ordine in cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="9d55c-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="9d55c-118">Nella tabella seguente viene illustrato un esempio di un set di attributi di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="9d55c-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="9d55c-119">Nome</span><span class="sxs-lookup"><span data-stu-id="9d55c-119">Name</span></span>                 | <span data-ttu-id="9d55c-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d55c-120">Type</span></span>         | <span data-ttu-id="9d55c-121">Valore stringa</span><span class="sxs-lookup"><span data-stu-id="9d55c-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="9d55c-122">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9d55c-122">msManipulationRule</span></span>   | <span data-ttu-id="9d55c-123">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9d55c-123">**VT\_BSTR**</span></span> | <span data-ttu-id="9d55c-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="9d55c-124">"@company.com"</span></span>   |
| <span data-ttu-id="9d55c-125">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9d55c-125">msManipulationRule</span></span>   | <span data-ttu-id="9d55c-126">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9d55c-126">**VT\_BSTR**</span></span> | <span data-ttu-id="9d55c-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="9d55c-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="9d55c-128">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9d55c-128">msManipulationRule</span></span>   | <span data-ttu-id="9d55c-129">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9d55c-129">**VT\_BSTR**</span></span> | <span data-ttu-id="9d55c-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="9d55c-130">"^.+@"</span></span>           |
| <span data-ttu-id="9d55c-131">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9d55c-131">msManipulationRule</span></span>   | <span data-ttu-id="9d55c-132">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="9d55c-132">**VT\_BSTR**</span></span> | <span data-ttu-id="9d55c-133">"guest@"</span><span class="sxs-lookup"><span data-stu-id="9d55c-133">"guest@"</span></span>         |
| <span data-ttu-id="9d55c-134">msManipulationTarget</span><span class="sxs-lookup"><span data-stu-id="9d55c-134">msManipulationTarget</span></span> | <span data-ttu-id="9d55c-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="9d55c-135">**VT\_I4**</span></span>   | <span data-ttu-id="9d55c-136">"1"</span><span class="sxs-lookup"><span data-stu-id="9d55c-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="9d55c-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d55c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d55c-138">Gerarchia del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="9d55c-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="9d55c-139">Attributi supportati da SDO</span><span class="sxs-lookup"><span data-stu-id="9d55c-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="9d55c-140">Creazione di un criterio di richiesta di connessione</span><span class="sxs-lookup"><span data-stu-id="9d55c-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="9d55c-141">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="9d55c-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="9d55c-142">**ISdoDictionaryOld**</span><span class="sxs-lookup"><span data-stu-id="9d55c-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="9d55c-143">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="9d55c-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 