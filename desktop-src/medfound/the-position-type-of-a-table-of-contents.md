---
description: Tipo di posizione di un sommario
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Tipo di posizione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310204"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="4e984-103">Tipo di posizione di un sommario</span><span class="sxs-lookup"><span data-stu-id="4e984-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="4e984-104">Alcuni metodi dell'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) hanno un parametro denominato *enumTocPosType* che dispone di un tipo di [**\_ \_ tipo POS del sommario enum**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span><span class="sxs-lookup"><span data-stu-id="4e984-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="4e984-105">Questo parametro specifica la posizione in un file multimediale in cui è archiviato un sommario.</span><span class="sxs-lookup"><span data-stu-id="4e984-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="4e984-106">Lo scopo è che il sommario possa essere archiviato nell'intestazione del file o nel corpo del file come oggetto di primo livello.</span><span class="sxs-lookup"><span data-stu-id="4e984-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="4e984-107">Questa funzionalità non è stata ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="4e984-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="4e984-108">Attualmente, le tabelle di contenuto possono essere archiviate solo come oggetti di primo livello, quindi è sempre necessario impostare il parametro *enumTocPosType* su **TOC \_ POS \_ TOPLEVELOBJECT**.</span><span class="sxs-lookup"><span data-stu-id="4e984-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="4e984-109">Se si imposta *enumTocPosType* su **TOC \_ POS \_ inheader**, il metodo restituirà **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="4e984-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="4e984-110">I metodi seguenti hanno un parametro *enumTocPosType* .</span><span class="sxs-lookup"><span data-stu-id="4e984-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="4e984-111">**GetTocCount**</span><span class="sxs-lookup"><span data-stu-id="4e984-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="4e984-112">**GetTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="4e984-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="4e984-113">**GetTocByType**</span><span class="sxs-lookup"><span data-stu-id="4e984-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="4e984-114">**AddToc**</span><span class="sxs-lookup"><span data-stu-id="4e984-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="4e984-115">**RemoveTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="4e984-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="4e984-116">**RemoveTocByType**</span><span class="sxs-lookup"><span data-stu-id="4e984-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="4e984-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e984-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e984-118">Guida per programmatori del parser Sommario</span><span class="sxs-lookup"><span data-stu-id="4e984-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



