---
description: ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232857"
---
# <a name="ice51"></a><span data-ttu-id="b293c-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="b293c-103">ICE51</span></span>

<span data-ttu-id="b293c-104">ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="b293c-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="b293c-105">È necessario specificare un titolo per una risorsa del tipo di carattere senza nome incorporato.</span><span class="sxs-lookup"><span data-stu-id="b293c-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="b293c-106">Solo i file di risorse del tipo di carattere. TTC,. ttf e. otf non richiedono un titolo, perché questi file contengono un nome incorporato.</span><span class="sxs-lookup"><span data-stu-id="b293c-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="b293c-107">Non specificare un titolo per una risorsa del tipo di carattere contenente un nome incorporato, perché il tipo di carattere viene registrato due volte dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b293c-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="b293c-108">**[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** ICE51 non controlla i file di risorse del tipo di carattere. otf.</span><span class="sxs-lookup"><span data-stu-id="b293c-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="b293c-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="b293c-109">Result</span></span>

<span data-ttu-id="b293c-110">ICE51 Invia un errore se sono presenti file di risorse del tipo. TTC,. ttf e. otf con titoli.</span><span class="sxs-lookup"><span data-stu-id="b293c-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="b293c-111">ICE51 pubblica un avviso se sono presenti altri file di risorse del tipo di carattere senza titolo.</span><span class="sxs-lookup"><span data-stu-id="b293c-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="b293c-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="b293c-112">Example</span></span>

<span data-ttu-id="b293c-113">ICE51 segnala l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="b293c-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="b293c-114">ICE51 segnala il seguente messaggio di errore per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="b293c-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="b293c-115">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b293c-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="b293c-116">File</span><span class="sxs-lookup"><span data-stu-id="b293c-116">File</span></span>  | <span data-ttu-id="b293c-117">FileName</span><span class="sxs-lookup"><span data-stu-id="b293c-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="b293c-118">Font1</span><span class="sxs-lookup"><span data-stu-id="b293c-118">Font1</span></span> | <span data-ttu-id="b293c-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="b293c-119">font1.ttf</span></span> |
| <span data-ttu-id="b293c-120">Font2</span><span class="sxs-lookup"><span data-stu-id="b293c-120">Font2</span></span> | <span data-ttu-id="b293c-121">font2. fon</span><span class="sxs-lookup"><span data-stu-id="b293c-121">font2.fon</span></span> |



 

[<span data-ttu-id="b293c-122">Tabella dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="b293c-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="b293c-123">file\_</span><span class="sxs-lookup"><span data-stu-id="b293c-123">File\_</span></span> | <span data-ttu-id="b293c-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="b293c-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="b293c-125">Font1</span><span class="sxs-lookup"><span data-stu-id="b293c-125">Font1</span></span>  | <span data-ttu-id="b293c-126">Un tipo di carattere molto interessante</span><span class="sxs-lookup"><span data-stu-id="b293c-126">A Really Cool Font</span></span> |
| <span data-ttu-id="b293c-127">Font2</span><span class="sxs-lookup"><span data-stu-id="b293c-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="b293c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b293c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b293c-129">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b293c-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



