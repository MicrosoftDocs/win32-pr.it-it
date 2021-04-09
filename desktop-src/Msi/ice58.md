---
description: ICE58 verifica che la tabella multimediale non includa più di 80 righe.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968099"
---
# <a name="ice58"></a><span data-ttu-id="80726-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="80726-103">ICE58</span></span>

<span data-ttu-id="80726-104">ICE58 verifica che la [tabella multimediale](media-table.md) non includa più di 80 righe.</span><span class="sxs-lookup"><span data-stu-id="80726-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="80726-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="80726-105">Result</span></span>

<span data-ttu-id="80726-106">Gli avvisi segnalati da ICE58 determinano l'esito negativo dell'installazione, a meno che il pacchetto non sia installato con Windows Installer 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="80726-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="80726-107">A partire da Windows Installer 2,0, viene rimossa la restrizione a più di 80 voci della tabella multimediale.</span><span class="sxs-lookup"><span data-stu-id="80726-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="80726-108">Se la proprietà di riepilogo dei conteggi delle [**pagine**](page-count-summary.md) del pacchetto è maggiore o uguale a 150, non viene generato alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="80726-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="80726-109">I pacchetti dello schema 200 o versioni successive possono essere installati solo da Windows Installer 2,0 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="80726-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="80726-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="80726-110">Example</span></span>

<span data-ttu-id="80726-111">ICE58 segnala gli errori e gli avvisi seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="80726-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="80726-112">Per correggere l'errore, eliminare le voci della tabella multimediale inutilizzata, consolidare le voci della tabella multimediale che fanno riferimento allo stesso supporto e riassemblare l'applicazione per ridurre i supporti necessari.</span><span class="sxs-lookup"><span data-stu-id="80726-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="80726-113">[Tabella media](media-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="80726-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="80726-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="80726-114">DiskId</span></span> | <span data-ttu-id="80726-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="80726-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="80726-116">1</span><span class="sxs-lookup"><span data-stu-id="80726-116">1</span></span>      | <span data-ttu-id="80726-117">10</span><span class="sxs-lookup"><span data-stu-id="80726-117">10</span></span>             |
| <span data-ttu-id="80726-118">2</span><span class="sxs-lookup"><span data-stu-id="80726-118">2</span></span>      | <span data-ttu-id="80726-119">20</span><span class="sxs-lookup"><span data-stu-id="80726-119">20</span></span>             |
| <span data-ttu-id="80726-120">...</span><span class="sxs-lookup"><span data-stu-id="80726-120">...</span></span>    | <span data-ttu-id="80726-121">...</span><span class="sxs-lookup"><span data-stu-id="80726-121">...</span></span>            |
| <span data-ttu-id="80726-122">81</span><span class="sxs-lookup"><span data-stu-id="80726-122">81</span></span>     | <span data-ttu-id="80726-123">810</span><span class="sxs-lookup"><span data-stu-id="80726-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="80726-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80726-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80726-125">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="80726-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



