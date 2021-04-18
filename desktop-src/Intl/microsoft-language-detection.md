---
description: Il servizio di rilevamento del linguaggio ELS è denominato Microsoft Rilevamento lingua. Questo servizio usa la tecnologia Microsoft brevettata per consentire alle applicazioni di rilevare la lingua in cui viene scritto un testo specifico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Rilevamento lingua Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308696"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="b9b56-104">Rilevamento lingua Microsoft</span><span class="sxs-lookup"><span data-stu-id="b9b56-104">Microsoft Language Detection</span></span>

<span data-ttu-id="b9b56-105">Il servizio di rilevamento del linguaggio ELS è denominato Microsoft Rilevamento lingua.</span><span class="sxs-lookup"><span data-stu-id="b9b56-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="b9b56-106">Questo servizio usa la tecnologia Microsoft brevettata per consentire alle applicazioni di rilevare la lingua in cui viene scritto un testo specifico.</span><span class="sxs-lookup"><span data-stu-id="b9b56-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="b9b56-107">Input per Microsoft Rilevamento lingua</span><span class="sxs-lookup"><span data-stu-id="b9b56-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="b9b56-108">L'input per il servizio Microsoft Rilevamento lingua è un testo UTF-16 (formato normalizzato C).</span><span class="sxs-lookup"><span data-stu-id="b9b56-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="b9b56-109">Il servizio deve determinare la lingua del testo.</span><span class="sxs-lookup"><span data-stu-id="b9b56-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="b9b56-110">Output di Microsoft Rilevamento lingua</span><span class="sxs-lookup"><span data-stu-id="b9b56-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="b9b56-111">Il servizio Microsoft Rilevamento lingua recupera un elenco di stringhe UTF-16 con terminazione del registro di sistema e con terminazione null, rappresentate dai rispettivi nomi, separate da delimitatori di carattere null.</span><span class="sxs-lookup"><span data-stu-id="b9b56-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="b9b56-112">L'elenco è ordinato in base alla pertinenza.</span><span class="sxs-lookup"><span data-stu-id="b9b56-112">The list is sorted by relevance.</span></span> <span data-ttu-id="b9b56-113">Per la maggior parte delle lingue vengono usati nomi neutri.</span><span class="sxs-lookup"><span data-stu-id="b9b56-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="b9b56-114">Tuttavia, per alcuni, ad esempio Sr-Cyrl, Sr-Latn, zh-Hant e zh-Hans, vengono usati nomi completi.</span><span class="sxs-lookup"><span data-stu-id="b9b56-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="b9b56-115">Operazione di Microsoft Rilevamento lingua</span><span class="sxs-lookup"><span data-stu-id="b9b56-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="b9b56-116">Il servizio Microsoft Rilevamento lingua controlla lo script Unicode del testo fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9b56-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="b9b56-117">Suddivide il testo in base agli script che rileva e quindi determina la lingua in cui viene scritto ogni segmento.</span><span class="sxs-lookup"><span data-stu-id="b9b56-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="b9b56-118">Se uno script indica una sola lingua, è garantita la presenza della lingua nell'elenco di lingue di output.</span><span class="sxs-lookup"><span data-stu-id="b9b56-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="b9b56-119">Il servizio usa un algoritmo brevettato per determinare la pertinenza di ogni lingua supportata.</span><span class="sxs-lookup"><span data-stu-id="b9b56-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="b9b56-120">GUID di Microsoft Rilevamento lingua</span><span class="sxs-lookup"><span data-stu-id="b9b56-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="b9b56-121">Il GUID per il servizio Microsoft Rilevamento lingua viene dichiarato in Elssrvc. h, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b9b56-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="b9b56-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9b56-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b56-123">Informazioni sui servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="b9b56-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



