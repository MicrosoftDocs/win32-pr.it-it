---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395227"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="98ffb-103">IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="98ffb-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="98ffb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98ffb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="98ffb-105">IAgentSpeechInputProperties consente di accedere alle proprietà di input vocale gestite dal server.</span><span class="sxs-lookup"><span data-stu-id="98ffb-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="98ffb-106">La maggior parte delle proprietà è di sola lettura per le applicazioni client, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="98ffb-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="98ffb-107">Il server Microsoft Agent restituisce i valori solo se è stato installato un motore di riconoscimento vocale compatibile ed è abilitato.</span><span class="sxs-lookup"><span data-stu-id="98ffb-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="98ffb-108">L'esecuzione di query su queste proprietà tenta di avviare il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="98ffb-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="98ffb-109">**Metodi nell'ordine Vtable**</span><span class="sxs-lookup"><span data-stu-id="98ffb-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="98ffb-110">Metodi IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="98ffb-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="98ffb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98ffb-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="98ffb-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="98ffb-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="98ffb-113">Restituisce un valore che indica se il motore di riconoscimento vocale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="98ffb-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="98ffb-114">**GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="98ffb-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="98ffb-115">Restituisce l'assegnazione di chiave corrente del tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="98ffb-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="98ffb-116">**GetListeningTip**</span><span class="sxs-lookup"><span data-stu-id="98ffb-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="98ffb-117">Restituisce un valore che indica se il suggerimento di ascolto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="98ffb-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="98ffb-118">I metodi [**Getinstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**semotore**](https://www.bing.com/search?q=**SetEngine**) (supportati nelle versioni precedenti di Microsoft Agent) sono ancora supportati per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="98ffb-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="98ffb-119">Tuttavia, i metodi non vengono sottoposti a Stub e non restituiscono valori utili.</span><span class="sxs-lookup"><span data-stu-id="98ffb-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="98ffb-120">Usare [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) per eseguire una query e impostare il motore di riconoscimento vocale da usare con il carattere.</span><span class="sxs-lookup"><span data-stu-id="98ffb-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="98ffb-121">Tenere presente che il motore deve corrispondere all'impostazione della lingua corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="98ffb-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




