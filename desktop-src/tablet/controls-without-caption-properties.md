---
description: Introduzione all'utilizzo di controlli senza proprietà didascalia per Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controlli senza proprietà didascalia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524378"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="dde4c-103">Controlli senza proprietà didascalia</span><span class="sxs-lookup"><span data-stu-id="dde4c-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="dde4c-104">Quando un controllo non ha una propria proprietà Caption, attenersi alla procedura seguente per assicurarsi che gli strumenti di accessibilità possano identificare i controlli:</span><span class="sxs-lookup"><span data-stu-id="dde4c-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="dde4c-105">Creare un controllo testo statico con un nome significativo e descrittivo.</span><span class="sxs-lookup"><span data-stu-id="dde4c-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="dde4c-106">Posizionare l'etichetta statica in modo che preceda immediatamente il controllo a cui si fa riferimento, in ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="dde4c-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="dde4c-107">Verificare che il testo dell'etichetta termini con i due punti, ad esempio "Settings:".</span><span class="sxs-lookup"><span data-stu-id="dde4c-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="dde4c-108">Posizionare il testo dell'etichetta immediatamente a sinistra o prima del controllo a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="dde4c-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="dde4c-109">Rendere invisibile il testo statico se non è appropriato visualizzarlo visivamente.</span><span class="sxs-lookup"><span data-stu-id="dde4c-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="dde4c-110">A tale scopo, assegnare l'attributo appropriato nello script della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dde4c-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="dde4c-111">Questo può essere appropriato quando il nome o la funzione di un controllo viene fornito visivamente tramite un metodo diverso dal controllo testo statico, ad esempio un elemento grafico o un pulsante di opzione correlato.</span><span class="sxs-lookup"><span data-stu-id="dde4c-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="dde4c-112">L'uso corretto dei controlli statici è l'unico modo per implementare correttamente le chiavi di accesso sottolineate per i controlli che non dispongono di etichette intrinseche.</span><span class="sxs-lookup"><span data-stu-id="dde4c-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="dde4c-113">Per ulteriori informazioni sull'utilizzo di controlli che non dispongono di proprietà didascalia, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="dde4c-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
