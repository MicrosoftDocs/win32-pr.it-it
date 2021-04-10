---
description: Scelta di un codec video
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Scelta di un codec video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225833"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="9ebb6-103">Scelta di un codec video (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="9ebb6-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="9ebb6-104">Il codificatore Windows Media Video 9 supporta tre categorie di output codificato: profilo principale, profilo avanzato e immagine.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="9ebb6-105">La categoria principale del profilo offre una compressione video generale per contenuti video complessi, ad esempio film o video musicali.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="9ebb6-106">Le funzionalità del profilo principale forniscono un'ampia gamma di impostazioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="9ebb6-107">È possibile usare il profilo principale per creare video con velocità in bit molto bassa per il recapito nei dispositivi palmari o, all'altra estremità dello spettro, è possibile usarlo per creare video ad alta definizione per Digital Cinema.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="9ebb6-108">L'enfasi degli algoritmi di codifica nel profilo principale è il contenuto video dinamico, ma sono adatti anche per altri contenuti video.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="9ebb6-109">Il profilo principale deve essere la categoria predefinita per il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="9ebb6-110">Per soddisfare esigenze specifiche, è possibile usare la categoria di profili avanzati, la categoria di immagini o un codificatore separato denominato codificatore Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="9ebb6-111">Nella tabella seguente sono elencate le quattro opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="9ebb6-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9ebb6-112">Scopo</span><span class="sxs-lookup"><span data-stu-id="9ebb6-112">Purpose</span></span></th>
<th><span data-ttu-id="9ebb6-113">Codec</span><span class="sxs-lookup"><span data-stu-id="9ebb6-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ebb6-114">Codifica video per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="9ebb6-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="9ebb6-115"><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="9ebb6-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="9ebb6-116">Main Profile</span><span class="sxs-lookup"><span data-stu-id="9ebb6-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebb6-117">Codifica di video o video ad alta definizione conformi allo standard VC-1 Advanced Profile SMPTE</span><span class="sxs-lookup"><span data-stu-id="9ebb6-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="9ebb6-118"><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="9ebb6-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="9ebb6-119">Profilo avanzato</span><span class="sxs-lookup"><span data-stu-id="9ebb6-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebb6-120">Conversione di immagini bitmap in video dinamici</span><span class="sxs-lookup"><span data-stu-id="9ebb6-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="9ebb6-121"><a href="windowsmediavideo9encoder.md">Codificatore Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="9ebb6-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="9ebb6-122">Immagine</span><span class="sxs-lookup"><span data-stu-id="9ebb6-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebb6-123">Codifica del computer-video dell'applicazione (acquisizione schermo) o altro video altamente statico</span><span class="sxs-lookup"><span data-stu-id="9ebb6-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="9ebb6-124"><a href="windowsmediavideo9screenencoder.md"><strong>Codificatore dello schermo Windows Media Video 9</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ebb6-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="9ebb6-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ebb6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ebb6-126">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="9ebb6-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



