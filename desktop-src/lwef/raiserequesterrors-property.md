---
title: Proprietà RaiseRequestErrors
description: Proprietà RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223859"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="fdc8d-103">Proprietà RaiseRequestErrors</span><span class="sxs-lookup"><span data-stu-id="fdc8d-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="fdc8d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdc8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fdc8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fdc8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fdc8d-106">Restituisce o imposta un valore che indica se vengono generati errori per le richieste.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="fdc8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="fdc8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fdc8d-108">\*agente \* \* *. RaiseRequestErrors*( \*  \[  =  *booleano* )\]</span><span class="sxs-lookup"><span data-stu-id="fdc8d-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="fdc8d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fdc8d-109">Part</span></span>      | <span data-ttu-id="fdc8d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc8d-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc8d-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="fdc8d-111">*boolean*</span></span> | <span data-ttu-id="fdc8d-112">Valore booleano che determina se vengono generati errori nelle richieste.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="fdc8d-113">**True**    (impostazione predefinita) vengono generati errori di richiesta.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="fdc8d-114">**False**     Gli errori di richiesta non vengono generati.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdc8d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdc8d-115">Remarks</span></span>

<span data-ttu-id="fdc8d-116">Questa proprietà consente di determinare se il server genera errori che si verificano con i metodi che supportano gli oggetti [**richiesta**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="fdc8d-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="fdc8d-117">Se, ad esempio, si specifica un nome di animazione che non esiste in un metodo [**Play**](play-method.md), il server genera un errore (visualizzando il messaggio di errore), a meno che questa proprietà non venga impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="fdc8d-118">Può essere utile per i linguaggi di programmazione che non forniscono il ripristino quando viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="fdc8d-119">Tuttavia, prestare attenzione quando si imposta questa proprietà su **false**, perché potrebbe essere più difficile trovare errori nel codice.</span><span class="sxs-lookup"><span data-stu-id="fdc8d-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

