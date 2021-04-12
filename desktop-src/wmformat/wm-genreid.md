---
title: WM/GenreID
description: L'attributo WM/GenreID contiene un identificatore di genere conforme al contenuto del tag TCON in ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato di Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398044"
---
# <a name="wmgenreid"></a><span data-ttu-id="38519-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="38519-104">WM/GenreID</span></span>

<span data-ttu-id="38519-105">L'attributo **WM/GenreID** contiene un identificatore di genere conforme al contenuto del tag TCON in id3v2.</span><span class="sxs-lookup"><span data-stu-id="38519-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="38519-106">Questo deve contenere l'ID del genere tra parentesi, seguito facoltativamente da un perfezionamento che descrive ulteriormente il genere.</span><span class="sxs-lookup"><span data-stu-id="38519-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="38519-107">Per ulteriori informazioni, vedere la specifica ID3v2.</span><span class="sxs-lookup"><span data-stu-id="38519-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="38519-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="38519-108">Global Constant</span></span>

<span data-ttu-id="38519-109">g \_ wszWMGenreID</span><span class="sxs-lookup"><span data-stu-id="38519-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="38519-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="38519-110">Data Type</span></span>

<span data-ttu-id="38519-111">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="38519-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="38519-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="38519-112">Remarks</span></span>

<span data-ttu-id="38519-113">L'attributo preferito per specificare un genere è [**WM/genre**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="38519-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="38519-114">Utilizzare questo attributo in modo preferenziale.</span><span class="sxs-lookup"><span data-stu-id="38519-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="38519-115">Se si modifica **WM/genre** o **WM/GenreID** in un file MP3, l'altro attributo verrà modificato in modo che corrisponda a.</span><span class="sxs-lookup"><span data-stu-id="38519-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="38519-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="38519-116">Example</span></span>



| <span data-ttu-id="38519-117">Tipo file</span><span class="sxs-lookup"><span data-stu-id="38519-117">File type</span></span> | <span data-ttu-id="38519-118">Valore di esempio</span><span class="sxs-lookup"><span data-stu-id="38519-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="38519-119">Audio</span><span class="sxs-lookup"><span data-stu-id="38519-119">Audio</span></span>     | <span data-ttu-id="38519-120">"(4) Eurodisco"</span><span class="sxs-lookup"><span data-stu-id="38519-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="38519-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38519-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38519-122">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="38519-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




