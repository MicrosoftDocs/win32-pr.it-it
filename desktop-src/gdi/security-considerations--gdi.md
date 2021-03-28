---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI. Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza. È invece possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considerazioni sulla sicurezza: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967947"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="b43dd-105">Considerazioni sulla sicurezza: GDI</span><span class="sxs-lookup"><span data-stu-id="b43dd-105">Security Considerations: GDI</span></span>

<span data-ttu-id="b43dd-106">In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI.</span><span class="sxs-lookup"><span data-stu-id="b43dd-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="b43dd-107">Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b43dd-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="b43dd-108">È invece possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.</span><span class="sxs-lookup"><span data-stu-id="b43dd-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="b43dd-109">In genere, GDI presenta pochi problemi di sicurezza perché gestisce la visualizzazione anziché l'input.</span><span class="sxs-lookup"><span data-stu-id="b43dd-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="b43dd-110">Tuttavia, di seguito sono riportate alcune problematiche da prendere in considerazione.</span><span class="sxs-lookup"><span data-stu-id="b43dd-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="b43dd-111">Bitmap, metafile e tipi di carattere sono strutture complesse che potrebbero essere danneggiate.</span><span class="sxs-lookup"><span data-stu-id="b43dd-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="b43dd-112">È consigliabile provare a verificare che questi elementi non siano danneggiati e da un'origine attendibile.</span><span class="sxs-lookup"><span data-stu-id="b43dd-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="b43dd-113">Un'applicazione può specificare il descrittore di sicurezza per alcune delle API di stampa e di spooling.</span><span class="sxs-lookup"><span data-stu-id="b43dd-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="b43dd-114">È necessario prestare attenzione quando si imposta il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b43dd-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b43dd-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b43dd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b43dd-116">Microsoft Security Central</span><span class="sxs-lookup"><span data-stu-id="b43dd-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="b43dd-117">Centro per sviluppatori dedicato alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="b43dd-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="b43dd-118">Security TechCenter</span><span class="sxs-lookup"><span data-stu-id="b43dd-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



