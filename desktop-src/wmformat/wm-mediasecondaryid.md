---
title: WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID contiene il GUID della classe multimediale secondaria.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato di Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397903"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="6da62-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="6da62-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="6da62-105">L'attributo **WM/MediaClassSecondaryID** contiene il GUID della classe multimediale secondaria.</span><span class="sxs-lookup"><span data-stu-id="6da62-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6da62-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="6da62-106">Global Constant</span></span>

<span data-ttu-id="6da62-107">g \_ wszWMMediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="6da62-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="6da62-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6da62-108">Data Type</span></span>

<span data-ttu-id="6da62-109">**\_GUID di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="6da62-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="6da62-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6da62-110">Remarks</span></span>

<span data-ttu-id="6da62-111">Questo attributo deve essere impostato su uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6da62-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="6da62-112">GUID classe secondaria</span><span class="sxs-lookup"><span data-stu-id="6da62-112">Secondary class GUID</span></span>                   | <span data-ttu-id="6da62-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6da62-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da62-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="6da62-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="6da62-115">Utilizzare per i file di audiolibro.</span><span class="sxs-lookup"><span data-stu-id="6da62-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="6da62-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="6da62-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="6da62-117">Utilizzare per i file audio che contengono parole pronunciate, ma che non sono libri audio.</span><span class="sxs-lookup"><span data-stu-id="6da62-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="6da62-118">Ad esempio, le routine della commedia di base.</span><span class="sxs-lookup"><span data-stu-id="6da62-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="6da62-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="6da62-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="6da62-120">Usare per i file audio correlati alle notizie.</span><span class="sxs-lookup"><span data-stu-id="6da62-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="6da62-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="6da62-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="6da62-122">Usare per i file audio con contenuto di talk show.</span><span class="sxs-lookup"><span data-stu-id="6da62-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="6da62-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="6da62-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="6da62-124">Usare per i file video correlati alle notizie.</span><span class="sxs-lookup"><span data-stu-id="6da62-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="6da62-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span><span class="sxs-lookup"><span data-stu-id="6da62-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="6da62-126">Da usare per i file video contenenti le esposizioni basate sul Web, i cortometraggi, i trailer di film e così via.</span><span class="sxs-lookup"><span data-stu-id="6da62-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="6da62-127">Si tratta dell'identificatore generale per gli intrattenimenti video che non rientrano in un'altra categoria.</span><span class="sxs-lookup"><span data-stu-id="6da62-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="6da62-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="6da62-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="6da62-129">Da usare per i file audio contenenti clip audio dei giochi.</span><span class="sxs-lookup"><span data-stu-id="6da62-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="6da62-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="6da62-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="6da62-131">Usare per i file audio che contengono brani completi dalle tracce audio del gioco.</span><span class="sxs-lookup"><span data-stu-id="6da62-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="6da62-132">Se nel file è codificata solo una parte di un brano, usare invece l'identificatore per i clip audio del gioco.</span><span class="sxs-lookup"><span data-stu-id="6da62-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="6da62-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="6da62-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="6da62-134">Da usare per i file video contenenti video musicali.</span><span class="sxs-lookup"><span data-stu-id="6da62-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="6da62-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="6da62-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="6da62-136">Da usare per i file video contenenti il video generale generale.</span><span class="sxs-lookup"><span data-stu-id="6da62-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="6da62-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="6da62-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="6da62-138">Da usare per i file video contenenti film di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6da62-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="6da62-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="6da62-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="6da62-140">Da usare per i file video contenenti le trasmissioni televisive.</span><span class="sxs-lookup"><span data-stu-id="6da62-140">Use for video files containing television shows.</span></span> <span data-ttu-id="6da62-141">Per gli show basati sul Web, usare l'identificatore più generico.</span><span class="sxs-lookup"><span data-stu-id="6da62-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="6da62-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="6da62-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="6da62-143">Da usare per i file video contenenti video aziendali.</span><span class="sxs-lookup"><span data-stu-id="6da62-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="6da62-144">Ad esempio, riunioni registrate o video di formazione.</span><span class="sxs-lookup"><span data-stu-id="6da62-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="6da62-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="6da62-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="6da62-146">Da usare per i file video contenenti video privati da fotografie.</span><span class="sxs-lookup"><span data-stu-id="6da62-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="6da62-147">Quando si specifica un identificatore di classe secondaria, il file deve contenere anche un attributo di identificatore di classe primario.</span><span class="sxs-lookup"><span data-stu-id="6da62-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="6da62-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6da62-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da62-149">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="6da62-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="6da62-150">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="6da62-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




