---
title: Attributi di tipo puntatore
description: Gli attributi seguenti specificano le caratteristiche dei puntatori.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL di IDL, attributi, tipo di puntatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714356"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="4ee21-104">Attributi di tipo puntatore</span><span class="sxs-lookup"><span data-stu-id="4ee21-104">Pointer Type Attributes</span></span>

<span data-ttu-id="4ee21-105">Gli attributi seguenti specificano le caratteristiche dei puntatori.</span><span class="sxs-lookup"><span data-stu-id="4ee21-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="4ee21-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="4ee21-106">Attribute</span></span>                                   | <span data-ttu-id="4ee21-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4ee21-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ee21-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4ee21-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="4ee21-109">Designa un puntatore come puntatore completo, con tutte le funzionalità di un puntatore del linguaggio C, incluso l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="4ee21-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="4ee21-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="4ee21-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="4ee21-111">Designa il tipo più semplice di puntatore in MIDL, ovvero uno che fornisce semplicemente l'indirizzo di alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="4ee21-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="4ee21-112">I puntatori di riferimento non possono mai essere null.</span><span class="sxs-lookup"><span data-stu-id="4ee21-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="4ee21-113">**unico**</span><span class="sxs-lookup"><span data-stu-id="4ee21-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="4ee21-114">Consente a un puntatore di essere null, ma non supporta l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="4ee21-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="4ee21-115">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="4ee21-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="4ee21-116">Applicato a un'interfaccia per specificare il tipo di puntatore predefinito per tutti i puntatori di tale interfaccia, ad eccezione dei puntatori di parametro di primo livello, che vengono automaticamente predefiniti per i puntatori [**ref**](ref.md) .</span><span class="sxs-lookup"><span data-stu-id="4ee21-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="4ee21-117">**IID \_ è**</span><span class="sxs-lookup"><span data-stu-id="4ee21-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="4ee21-118">Fornisce l'identificatore di interfaccia dell'interfaccia COM che rappresenta l'oggetto dell'indicatore di misura.</span><span class="sxs-lookup"><span data-stu-id="4ee21-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="4ee21-119">**string**</span><span class="sxs-lookup"><span data-stu-id="4ee21-119">**string**</span></span>](string.md)                    | <span data-ttu-id="4ee21-120">Specifica che il puntatore punta a una stringa.</span><span class="sxs-lookup"><span data-stu-id="4ee21-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




