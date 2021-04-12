---
title: Altri motori di riconoscimento vocale compatibili con Microsoft Agent
description: Altri motori di riconoscimento vocale compatibili con Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398668"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a><span data-ttu-id="0e1c0-103">Altri motori di riconoscimento vocale compatibili con Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="0e1c0-103">Other Speech Engines Compatible with Microsoft Agent</span></span>

<span data-ttu-id="0e1c0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0e1c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0e1c0-105">Oltre ai motori di riconoscimento vocale Microsoft forniti con e supportano Microsoft Agent, diverse aziende offrono anche motori di riconoscimento vocale con supporto per Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-105">In addition to the Microsoft speech engines that are provided with and support Microsoft Agent, a number of companies also offer speech engines with support for Microsoft Agent.</span></span> <span data-ttu-id="0e1c0-106">Questa pagina offre una breve panoramica di tali motori che potrebbero essere disponibili in inglese (Stati Uniti) e in altri linguaggi.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-106">This page gives you a brief overview of such engines that may be available in U.S. English and other languages.</span></span> <span data-ttu-id="0e1c0-107">Le informazioni su come installare e accedere, nonché la licenza e la ridistribuzione dei motori sono reperibili nei siti Web.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-107">Information about how to install and access, as well as license and redistribute the engines can be found at their websites.</span></span>

<span data-ttu-id="0e1c0-108">Quando si usa un motore di sintesi vocale di terze parti, è necessario installare anche i file binari di runtime di Microsoft SAPI 4.0, in modo che i motori vengano enumerati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-108">When using any third-party speech engine, you also need to install Microsoft SAPI 4.0a runtime binaries so that the engines are enumerated properly.</span></span> <span data-ttu-id="0e1c0-109">Dalla pagina Web è possibile includere il tag seguente per attivare un download automatica del Speech API:</span><span class="sxs-lookup"><span data-stu-id="0e1c0-109">From your webpage you can include the following tag to trigger an autodownload of the Speech API:</span></span>

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

<span data-ttu-id="0e1c0-110">Per altre informazioni sui file binari del runtime di SAPI, vedere il [sito Web del gruppo di riconoscimento vocale Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="0e1c0-110">For more information about the SAPI runtime binaries, refer to the [Microsoft Speech group's website](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="0e1c0-111">Microsoft Agent installa anche i file binari di runtime SAPI con il motore di riconoscimento vocale Microsoft, il pannello di controllo vocale e l'editor dei caratteri dell'agente.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-111">Microsoft Agent also installs the SAPI runtime binaries with the Microsoft Speech Recognition Engine, the Speech Control Panel, and the Agent Character Editor.</span></span>

<span data-ttu-id="0e1c0-112">Si noti che questi collegamenti puntano a server che non sono sotto il controllo Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-112">Please note that these links point to servers that are not under Microsoft control.</span></span> <span data-ttu-id="0e1c0-113">Leggi l'informativa [ufficiale](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) Microsoft relativa ad altri server.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-113">Please read the Microsoft [official statement](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) regarding other servers.</span></span> <span data-ttu-id="0e1c0-114">Microsoft non approva il contenuto né il software fornito in questi siti Web.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-114">Microsoft does not endorse the content nor the software provided at these websites.</span></span> <span data-ttu-id="0e1c0-115">Tutte le domande tecniche e di supporto devono essere indirizzate anche ai fornitori dei motori e non a Microsoft o al team di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-115">All technical and support questions should also be directed to the suppliers of the engines and not to Microsoft or the Microsoft Agent team.</span></span>

<span data-ttu-id="0e1c0-116">**Motore di sintesi vocale di digalo**</span><span class="sxs-lookup"><span data-stu-id="0e1c0-116">**Digalo Text-To-Speech Engine**</span></span>

<span data-ttu-id="0e1c0-117">Digalo è un motore TTS conveniente progettato per gli utenti finali e gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-117">Digalo is an affordable TTS engine designed for end-users and developers.</span></span> <span data-ttu-id="0e1c0-118">Il motore di è disponibile in diverse lingue: francese, tedesco, portoghese (Brasile), spagnolo, russo, Regno Unito e inglese (Stati Uniti), con lingue italiane, polacche e altre lingue presto disponibili.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-118">The engine is offered in a number of languages: French, German, Portuguese (Brazil), Spanish, Russian, and UK and U.S. English, with Italian, Polish, and other languages coming soon.</span></span> <span data-ttu-id="0e1c0-119">Sono inoltre disponibili informazioni per gli sviluppatori, nonché informazioni dettagliate sulla registrazione e sui programmi affiliati dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-119">Developer information, as well as details on end-user registration and affiliate programs, is also available.</span></span>

<span data-ttu-id="0e1c0-120">**Motore di sintesi vocale Elan**</span><span class="sxs-lookup"><span data-stu-id="0e1c0-120">**Elan Speech Engine**</span></span>

<span data-ttu-id="0e1c0-121">Il motore di sintesi vocale Elan usa la tecnologia di sintesi vocale di Elan ed è disponibile in sette lingue: francese, tedesco, portoghese (Brasile), spagnolo, russo, Regno Unito e inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="0e1c0-121">Elan Speech Engine uses Elan's Text To Speech technology and is available in seven languages: French, German, Portuguese (Brazil), Spanish, Russian, UK and U.S. English.</span></span>

<span data-ttu-id="0e1c0-122">**IBM ViaVoice Outloud**</span><span class="sxs-lookup"><span data-stu-id="0e1c0-122">**IBM ViaVoice Outloud**</span></span>

<span data-ttu-id="0e1c0-123">IBM ha sviluppato diversi caratteri degli agenti Microsoft per l'uso con ViaVoice Outloud.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-123">IBM has developed several Microsoft Agent characters for use with ViaVoice Outloud.</span></span> <span data-ttu-id="0e1c0-124">IBM ViaVoice Outloud è una tecnologia di sintesi vocale (sintesi vocale) ed è disponibile in francese, tedesco, italiano, spagnolo, inglese (Regno Unito) e inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="0e1c0-124">IBM ViaVoice Outloud is a text-to-speech (speech synthesis) technology and is available in French, German, Italian, Spanish, UK English and U.S. English.</span></span> <span data-ttu-id="0e1c0-125">In combinazione con Microsoft Agent, è possibile creare applicazioni vivaci in molte lingue ed estendere le opportunità di vendita ai nuovi mercati in tutto il mondo.</span><span class="sxs-lookup"><span data-stu-id="0e1c0-125">When combined with Microsoft Agent, you can create vibrant applications in many languages and extend your sales opportunities to new worldwide markets.</span></span>

 

 




