---
description: Il servizio di rilevamento script ELS è denominato rilevamento script Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Rilevamento script Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130311"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="7ed0c-103">Rilevamento script Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ed0c-103">Microsoft Script Detection</span></span>

<span data-ttu-id="7ed0c-104">Il servizio di rilevamento script ELS è denominato rilevamento script Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="7ed0c-105">Questo servizio consente alle applicazioni di rilevare gli script in cui viene scritto il testo.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="7ed0c-106">La controparte NLS (National Language Support) di un servizio di rilevamento script è la funzione [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) .</span><span class="sxs-lookup"><span data-stu-id="7ed0c-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="7ed0c-107">Il servizio ELS, tuttavia, recupera inoltre gli intervalli di testo che appartengono a ogni sistema di scrittura.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="7ed0c-108">Input per il rilevamento di script Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ed0c-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="7ed0c-109">L'input per il servizio rilevamento script Microsoft è un testo UTF-16 per il quale il servizio determina gli intervalli di script.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="7ed0c-110">Output del rilevamento di script Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ed0c-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="7ed0c-111">L'output del servizio Microsoft Script Detection è una matrice di intervalli, ognuno dei quali contiene una stringa UTF-16 con terminazione null con il nome Unicode specificato del sistema di scrittura associato.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="7ed0c-112">Il servizio segnala i caratteri comuni (Rachele) e ereditato (Qaai) normali come appartenenti all'intervallo di script precedente.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="7ed0c-113">L'inizio dei caratteri comuni e ereditati viene segnalato come appartenente al successivo intervallo di script.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="7ed0c-114">Se tutti i caratteri nel testo di input sono comuni o ereditati, l'output del servizio è un singolo intervallo con la stringa vuota come dati.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="7ed0c-115">Operazione di rilevamento script Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ed0c-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="7ed0c-116">Il servizio Microsoft Script Detection esegue il mapping dei punti di codice appartenenti all'intervallo comune al sistema di scrittura precedente.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="7ed0c-117">In alternativa, il servizio può eseguire il mapping dei punti di codice al sistema di scrittura successivo se i punti di codice si trovano all'inizio della stringa di input.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="7ed0c-118">Non è necessario che l'applicazione gestisca l'intervallo comune.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="7ed0c-119">GUID rilevamento script Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ed0c-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="7ed0c-120">Il GUID per il servizio Microsoft Rilevamento lingua viene dichiarato in Elssrvc. h, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="7ed0c-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="7ed0c-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ed0c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed0c-122">Informazioni sui servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="7ed0c-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



