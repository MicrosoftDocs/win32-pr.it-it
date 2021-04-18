---
title: Gestione della tastiera nei controlli
description: Gestione della tastiera nei controlli
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298935"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="92ca2-103">Gestione della tastiera nei controlli</span><span class="sxs-lookup"><span data-stu-id="92ca2-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="92ca2-104">Il supporto per la gestione della tastiera per le funzionalità seguenti è fortemente consigliato, anche se è noto che non è applicabile a tutti i contenitori.</span><span class="sxs-lookup"><span data-stu-id="92ca2-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="92ca2-105">Supporto per i \_ bit di stato OLEMISC ACTSLIKELABEL e OLEMISC \_ ACTSLIKEBUTTON.</span><span class="sxs-lookup"><span data-stu-id="92ca2-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="92ca2-106">Implementando la proprietà di ambiente DisplayAsDefault, se esistente, può restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="92ca2-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="92ca2-107">Implementazione della gestione delle schede, incluso l'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="92ca2-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="92ca2-108">Alcuni contenitori utilizzeranno i controlli ActiveX negli scenari tradizionali dei documenti composti.</span><span class="sxs-lookup"><span data-stu-id="92ca2-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="92ca2-109">Un foglio di calcolo, ad esempio, può consentire a un utente di incorporare un controllo ActiveX in un foglio di lavoro.</span><span class="sxs-lookup"><span data-stu-id="92ca2-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="92ca2-110">In questi scenari, il contenitore eseguirebbe la gestione della tastiera in modo diverso, perché l'interfaccia della tastiera deve rimanere coerente con le aspettative dell'utente di un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="92ca2-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="92ca2-111">La documentazione relativa a tali prodotti deve informare gli utenti sulle differenze nella gestione dei controlli in questi diversi scenari.</span><span class="sxs-lookup"><span data-stu-id="92ca2-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="92ca2-112">Gli altri contenitori dovrebbero tentare di rispettare correttamente le funzionalità sopra indicate, inclusa la gestione dei tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="92ca2-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92ca2-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92ca2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ca2-114">Contenitori</span><span class="sxs-lookup"><span data-stu-id="92ca2-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




