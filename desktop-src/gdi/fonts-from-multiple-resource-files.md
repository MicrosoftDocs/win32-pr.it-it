---
description: Tipi di carattere da più file di risorse
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Tipi di carattere da più file di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996449"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="afe4d-103">Tipi di carattere da più file di risorse</span><span class="sxs-lookup"><span data-stu-id="afe4d-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="afe4d-104">In genere, un tipo di carattere è contenuto in un singolo file di risorse del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="afe4d-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="afe4d-105">Tuttavia, le informazioni relative ad alcuni tipi di carattere vengono distribuite tra diversi file.</span><span class="sxs-lookup"><span data-stu-id="afe4d-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="afe4d-106">Ad esempio, digitare 1 più tipi di carattere Master richiedono due file:</span><span class="sxs-lookup"><span data-stu-id="afe4d-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="afe4d-107">. PFM per le metriche dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="afe4d-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="afe4d-108">. PFB per i bit del carattere</span><span class="sxs-lookup"><span data-stu-id="afe4d-108">.pfb for the font bits</span></span>

<span data-ttu-id="afe4d-109">Per aggiungere un tipo di carattere da più file al sistema, usare le funzioni [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="afe4d-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="afe4d-110">Il parametro *lpszFileName* in queste funzioni deve puntare a una stringa che contiene i nomi file separati dalla barra verticale o dalla pipe ( \| ).</span><span class="sxs-lookup"><span data-stu-id="afe4d-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="afe4d-111">Per specificare, ad esempio, abcxxxxx. PFM e abcxxxxx. PFB per un tipo di carattere 1, utilizzare la stringa "abcxxxxx. PFM \| abcxxxxx. pfb".</span><span class="sxs-lookup"><span data-stu-id="afe4d-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="afe4d-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differisce da [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in quanto l'applicazione che chiama **AddFontResourceEx** può specificare il tipo di carattere come privato o non enumerabile.</span><span class="sxs-lookup"><span data-stu-id="afe4d-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="afe4d-113">Per aggiungere un tipo di carattere da un'immagine di memoria, usare [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="afe4d-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="afe4d-114">Questo consente a un'applicazione di usare un tipo di carattere incorporato in un documento o in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="afe4d-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="afe4d-115">Per rimuovere un tipo di carattere che proviene da più file di risorse, chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) o [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), a seconda della funzione utilizzata per aggiungere il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="afe4d-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="afe4d-116">È necessario specificare gli stessi flag utilizzati per aggiungere il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="afe4d-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="afe4d-117">Per rimuovere un tipo di carattere aggiunto da un'immagine di memoria, utilizzare [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="afe4d-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="afe4d-118">L'uso di un tipo di carattere che deriva da più file di risorse del tipo di carattere è identico a quello di un singolo file di risorse.</span><span class="sxs-lookup"><span data-stu-id="afe4d-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
