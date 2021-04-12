---
title: Parametro MSWMExt (deprecato)
description: Parametro MSWMExt (deprecato)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metafile di Windows Media, parametro MSWMExt
- Metafile, parametro MSWMExt
- Parametro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398666"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="ca4ec-106">Parametro MSWMExt (deprecato)</span><span class="sxs-lookup"><span data-stu-id="ca4ec-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="ca4ec-107">Il parametro *MSWMExt* indica a un programma client il formato di un file a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="ca4ec-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="ca4ec-108">**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ca4ec-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="ca4ec-109">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="ca4ec-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="ca4ec-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca4ec-110">Remarks</span></span>

<span data-ttu-id="ca4ec-111">I programmi client a volte usano un'estensione di file o un tipo MIME per determinare se eseguire il rendering di un file multimediale come flusso, eseguire il rendering del file dopo un download completo o rifiutare il rendering del file.</span><span class="sxs-lookup"><span data-stu-id="ca4ec-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="ca4ec-112">Se un programma client non è in grado di determinare come gestire un file multimediale in base all'estensione del nome di file o al tipo MIME, può determinare come trattare il file esaminando il parametro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="ca4ec-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="ca4ec-113">Ad esempio, il client potrebbe trattare il file come se disponesse di un'estensione uguale al valore del parametro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="ca4ec-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="ca4ec-114">Per ulteriori informazioni sui tipi MIME e sulle estensioni dei nomi di file, vedere [estensioni di file](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ca4ec-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="ca4ec-115">Per ulteriori informazioni sul parametro *MSWMExt* , vedere l'articolo [236895](https://support.microsoft.com/kb/236895) della Microsoft Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="ca4ec-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca4ec-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca4ec-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca4ec-117">**Versioni precedenti dei file di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="ca4ec-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




