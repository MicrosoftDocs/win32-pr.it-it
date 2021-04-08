---
description: ICE15 verifica che il tipo di contenuto e i riferimenti all'estensione nelle tabelle MIME e Extension siano reciproci. La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione che la tabella di estensione fa riferimento allo stesso tipo di contenuto.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057811"
---
# <a name="ice15"></a><span data-ttu-id="a961b-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="a961b-104">ICE15</span></span>

<span data-ttu-id="a961b-105">ICE15 verifica che il tipo di contenuto e i riferimenti all'estensione nelle tabelle [MIME](mime-table.md) e [Extension](extension-table.md) siano reciproci.</span><span class="sxs-lookup"><span data-stu-id="a961b-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="a961b-106">La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione che la tabella di estensione fa riferimento allo stesso tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="a961b-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="a961b-107">Più estensioni possono fare riferimento allo stesso tipo MIME, purché il tipo MIME faccia riferimento a una delle estensioni.</span><span class="sxs-lookup"><span data-stu-id="a961b-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="a961b-108">Più tipi MIME possono fare riferimento alla stessa estensione, purché l'estensione faccia riferimento a uno dei tipi MIME.</span><span class="sxs-lookup"><span data-stu-id="a961b-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="a961b-109">Si noti che ogni volta che un MIME fa riferimento a un'estensione, tale estensione non può avere la colonna MIME della \_ tabella di estensione impostata su null.</span><span class="sxs-lookup"><span data-stu-id="a961b-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="a961b-110">Risultato</span><span class="sxs-lookup"><span data-stu-id="a961b-110">Result</span></span>

<span data-ttu-id="a961b-111">ICE15 Invia un errore se il tipo di contenuto e i riferimenti all'estensione non sono reciproci.</span><span class="sxs-lookup"><span data-stu-id="a961b-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="a961b-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a961b-112">Example</span></span>

<span data-ttu-id="a961b-113">ICE15 invia due messaggi di errore per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="a961b-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="a961b-114">Il tipo di contenuto test/x-flaps nella tabella MIME fa riferimento alla TST dell'estensione, ma il TST di estensione nella tabella di estensione fa riferimento a flap/x-flaps.</span><span class="sxs-lookup"><span data-stu-id="a961b-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="a961b-115">Questo non è reciproco.</span><span class="sxs-lookup"><span data-stu-id="a961b-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="a961b-116">Il tipo di contenuto flaps/x-flaps fa riferimento all'estensione FLP, ma tale estensione include una voce null nella \_ colonna MIME della tabella di estensione.</span><span class="sxs-lookup"><span data-stu-id="a961b-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="a961b-117">[Tabella MIME](mime-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a961b-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="a961b-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="a961b-118">ContentType</span></span>   | <span data-ttu-id="a961b-119">Estensione\_</span><span class="sxs-lookup"><span data-stu-id="a961b-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="a961b-120">test/x-test</span><span class="sxs-lookup"><span data-stu-id="a961b-120">test/x-test</span></span>   | <span data-ttu-id="a961b-121">TST</span><span class="sxs-lookup"><span data-stu-id="a961b-121">tst</span></span>         |
| <span data-ttu-id="a961b-122">Flap/x-flap</span><span class="sxs-lookup"><span data-stu-id="a961b-122">flaps/x-flaps</span></span> | <span data-ttu-id="a961b-123">FLP</span><span class="sxs-lookup"><span data-stu-id="a961b-123">flp</span></span>         |



 

<span data-ttu-id="a961b-124">[Tabella di estensione](extension-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a961b-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="a961b-125">Estensione</span><span class="sxs-lookup"><span data-stu-id="a961b-125">Extension</span></span> | <span data-ttu-id="a961b-126">MIME\_</span><span class="sxs-lookup"><span data-stu-id="a961b-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="a961b-127">TST</span><span class="sxs-lookup"><span data-stu-id="a961b-127">tst</span></span>       | <span data-ttu-id="a961b-128">Flap/x-flap</span><span class="sxs-lookup"><span data-stu-id="a961b-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="a961b-129">FLP</span><span class="sxs-lookup"><span data-stu-id="a961b-129">flp</span></span>       | <span data-ttu-id="a961b-130">Null</span><span class="sxs-lookup"><span data-stu-id="a961b-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="a961b-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a961b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a961b-132">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="a961b-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



