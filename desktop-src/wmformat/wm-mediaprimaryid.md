---
title: WM/MediaClassPrimaryID
description: L'attributo WM/MediaClassPrimaryID contiene il GUID della classe multimediale primaria.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato di Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857578"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="a2635-104">WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="a2635-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="a2635-105">L'attributo **WM/MediaClassPrimaryID** contiene il GUID della classe multimediale primaria.</span><span class="sxs-lookup"><span data-stu-id="a2635-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a2635-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a2635-106">Global Constant</span></span>

<span data-ttu-id="a2635-107">g \_ wszWMMediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="a2635-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="a2635-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a2635-108">Data Type</span></span>

<span data-ttu-id="a2635-109">**\_GUID di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a2635-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2635-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2635-110">Remarks</span></span>

<span data-ttu-id="a2635-111">Questo attributo deve essere impostato su uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a2635-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="a2635-112">GUID della classe primaria</span><span class="sxs-lookup"><span data-stu-id="a2635-112">Primary class GUID</span></span>                     | <span data-ttu-id="a2635-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2635-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a2635-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="a2635-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="a2635-115">Da usare per i file musicali.</span><span class="sxs-lookup"><span data-stu-id="a2635-115">Use for music files.</span></span> <span data-ttu-id="a2635-116">Non usare per audio che non sia musica.</span><span class="sxs-lookup"><span data-stu-id="a2635-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="a2635-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="a2635-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="a2635-118">Da usare per i file video.</span><span class="sxs-lookup"><span data-stu-id="a2635-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="a2635-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="a2635-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="a2635-120">Utilizzare per i file audio che non sono musica.</span><span class="sxs-lookup"><span data-stu-id="a2635-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="a2635-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="a2635-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="a2635-122">Utilizzare per i file che non sono audio o video.</span><span class="sxs-lookup"><span data-stu-id="a2635-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="a2635-123">Quando si specifica un identificatore di classe primario, è necessario impostare anche un identificatore di classe secondaria per chiarire il tipo di contenuto nel file.</span><span class="sxs-lookup"><span data-stu-id="a2635-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2635-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2635-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2635-125">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="a2635-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="a2635-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="a2635-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




