---
title: Elementi obbligatori
description: Elementi obbligatori
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Interfacce di Windows Media Player Mobile, elementi
- interfacce, elementi
- file di definizione dell'interfaccia, elementi
- elementi, file di definizione dell'interfaccia
- elementi, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710876"
---
# <a name="required-elements"></a><span data-ttu-id="74e31-108">Elementi obbligatori</span><span class="sxs-lookup"><span data-stu-id="74e31-108">Required Elements</span></span>

<span data-ttu-id="74e31-109">È necessario specificare gli elementi seguenti nel file di definizione dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="74e31-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="74e31-110">**Intestazione.**</span><span class="sxs-lookup"><span data-stu-id="74e31-110">**Header.**</span></span> <span data-ttu-id="74e31-111">L'intestazione del file di definizione dell'interfaccia principale è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="74e31-111">The main skin definition file header is required.</span></span> <span data-ttu-id="74e31-112">Per informazioni sulla versione dell'intestazione, vedere la tabella nella sezione [creazione di un file di definizione dell'interfaccia](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="74e31-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="74e31-113">**Sezione Descrizione.**</span><span class="sxs-lookup"><span data-stu-id="74e31-113">**Description section.**</span></span> <span data-ttu-id="74e31-114">La sezione Descrizione è obbligatoria per la creazione di interfacce per Windows Media Player 9 serie per Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="74e31-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="74e31-115">Deve essere la prima sezione del file di definizione dell'interfaccia e deve specificare valori validi per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="74e31-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="74e31-116">La specifica di un valore per l'orientamento è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="74e31-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="74e31-117">**Sezione bitmap.**</span><span class="sxs-lookup"><span data-stu-id="74e31-117">**Bitmaps section.**</span></span> <span data-ttu-id="74e31-118">La sezione bitmap è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="74e31-118">The Bitmaps section is required.</span></span> <span data-ttu-id="74e31-119">Inoltre, la sezione bitmap deve specificare nomi validi per i file di sfondo, disabilitato, push, area e immagine superata.</span><span class="sxs-lookup"><span data-stu-id="74e31-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="74e31-120">**file di immagine.**</span><span class="sxs-lookup"><span data-stu-id="74e31-120">**Image files.**</span></span> <span data-ttu-id="74e31-121">Come parte dell'interfaccia, è necessario fornire i file di sfondo, disabilitato, di push, di area e di immagine con privilegi avanzati.</span><span class="sxs-lookup"><span data-stu-id="74e31-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="74e31-122">Se si creano interfacce per Windows Media Player 10 mobile o versioni successive, non è necessario includere i file di area o di immagine super.</span><span class="sxs-lookup"><span data-stu-id="74e31-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="74e31-123">Se si crea un'interfaccia con solo immagini definite, l'interfaccia sarà visibile, ma non offrirà alcuna funzionalità significativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="74e31-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="74e31-124">Se si decide di creare un'interfaccia senza pulsanti, ad esempio per impedire all'utente di ignorare un determinato contenuto, tenere presente che potrebbe essere ancora possibile eseguire il mapping delle funzionalità ai pulsanti hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74e31-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="74e31-125">I file Thumb sono obbligatori e i TrackBar non possono essere usati senza Thumb.</span><span class="sxs-lookup"><span data-stu-id="74e31-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74e31-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74e31-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74e31-127">**File di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="74e31-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




