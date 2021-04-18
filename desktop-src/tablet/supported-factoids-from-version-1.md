---
description: La piattaforma Tablet PC supporta un numero di factoids che vengono utilizzati per aumentare l'accuratezza del riconoscimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids supportati dalla versione 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319140"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="e074f-103">Factoids supportati dalla versione 1</span><span class="sxs-lookup"><span data-stu-id="e074f-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="e074f-104">\[Tenere presente che la descrizione di factoids supportata nella versione 1 del Software Development Kit (SDK) di Microsoft Windows XP Tablet PC Edition è ancora supportata dai sistemi di riconoscimento, ma è consigliabile che tutti i nuovi sviluppatori (per i riconoscitori dello script latino) usino i valori definiti nell'enumerazione [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]</span><span class="sxs-lookup"><span data-stu-id="e074f-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="e074f-105">La piattaforma Tablet PC supporta un numero di factoids che vengono utilizzati per aumentare l'accuratezza del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="e074f-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="e074f-106">Quando si usa factoids, è importante che l'input previsto corrisponda esattamente alla definizione del controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="e074f-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="e074f-107">Se l'input non corrisponde alla definizione del controllo del controllo, l'accuratezza del riconoscimento soffre.</span><span class="sxs-lookup"><span data-stu-id="e074f-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="e074f-108">Se, ad esempio, il controllo di controllo **numerico** è impostato e l'utente immette lettere, l'accuratezza del riconoscimento per le lettere è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e074f-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="e074f-109">Alcuni factoids, ad esempio la **posta elettronica** e la **cifra**, sono quasi identici in tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="e074f-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="e074f-110">Altri factoids, ad esempio **telefono** e **Cap**, variano in base alla lingua.</span><span class="sxs-lookup"><span data-stu-id="e074f-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="e074f-111">Esaminare il formato di ogni controllo oggetto per la lingua in uso.</span><span class="sxs-lookup"><span data-stu-id="e074f-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="e074f-112">Un elenco di formati per ogni controllo oggetto in ogni lingua è disponibile nelle tabelle degli argomenti che seguono questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e074f-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="e074f-113">Esiste una differenza sottile ma importante tra factoids per le lingue occidentali e factoids per le lingue asiatiche orientali.</span><span class="sxs-lookup"><span data-stu-id="e074f-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="e074f-114">Factoids per le lingue occidentali vengono implementate usando espressioni che descrivono il risultato desiderato.</span><span class="sxs-lookup"><span data-stu-id="e074f-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="e074f-115">Il riconoscimento viene quindi distorto per produrre risultati corrispondenti a questa espressione.</span><span class="sxs-lookup"><span data-stu-id="e074f-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="e074f-116">Factoids per le lingue asiatiche orientali vengono implementate specificando un intervallo di caratteri Unicode accettabile.</span><span class="sxs-lookup"><span data-stu-id="e074f-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="e074f-117">Ad esempio, il controllo della **Data** per le lingue asiatiche orientali accetta solo caratteri Unicode in un determinato intervallo.</span><span class="sxs-lookup"><span data-stu-id="e074f-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="e074f-118">Factoids per le lingue occidentali includono factoids per la lingua inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo.</span><span class="sxs-lookup"><span data-stu-id="e074f-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="e074f-119">Factoids per le lingue asiatiche orientali includono factoids per il cinese (semplificato), cinese (tradizionale), giapponese e coreano.</span><span class="sxs-lookup"><span data-stu-id="e074f-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="e074f-120">Nelle sezioni seguenti vengono illustrati i formati supportati per ogni controllo oggetto in ogni lingua:</span><span class="sxs-lookup"><span data-stu-id="e074f-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="e074f-121">Factoids comuni tra lingue diverse</span><span class="sxs-lookup"><span data-stu-id="e074f-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="e074f-122">Factoids per le lingue occidentali</span><span class="sxs-lookup"><span data-stu-id="e074f-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="e074f-123">Factoids per le lingue asiatiche orientali</span><span class="sxs-lookup"><span data-stu-id="e074f-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="e074f-124">Se si prevede un input diverso dai formati elencati nelle tabelle di queste sezioni, non usare un controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="e074f-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="e074f-125">Inoltre, factoids sono incorporati nel riconoscimento per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="e074f-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="e074f-126">Non è possibile usare factoids da un linguaggio con un riconoscimento da un altro linguaggio.</span><span class="sxs-lookup"><span data-stu-id="e074f-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="e074f-127">Non è ad esempio possibile utilizzare il controllo del **telefono** francese con un riconoscimento giapponese.</span><span class="sxs-lookup"><span data-stu-id="e074f-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e074f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e074f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e074f-129">**Costanti controllo oggetto**</span><span class="sxs-lookup"><span data-stu-id="e074f-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="e074f-130">[Classe Microsoft. Ink. controllore](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e074f-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
