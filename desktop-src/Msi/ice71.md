---
description: ICE71 verifica che la tabella media includa una voce con DiskID uguale a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968234"
---
# <a name="ice71"></a><span data-ttu-id="d5b7c-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="d5b7c-103">ICE71</span></span>

<span data-ttu-id="d5b7c-104">ICE71 verifica che la [tabella media](media-table.md) includa una voce con DiskID uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="d5b7c-105">(Windows Installer presuppone che il pacchetto MSI si trovi sul disco 1.)</span><span class="sxs-lookup"><span data-stu-id="d5b7c-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="d5b7c-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="d5b7c-106">Result</span></span>

<span data-ttu-id="d5b7c-107">ICE71 restituisce un errore se la tabella media non contiene una voce con DiskID uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="d5b7c-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="d5b7c-108">Example</span></span>

<span data-ttu-id="d5b7c-109">ICE71 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="d5b7c-110">T0 correggere l'errore, modificare il DiskID della voce in cui il pacchetto viene archiviato in 1.</span><span class="sxs-lookup"><span data-stu-id="d5b7c-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="d5b7c-111">[Tabella media](media-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="d5b7c-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="d5b7c-112">DiskId</span><span class="sxs-lookup"><span data-stu-id="d5b7c-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="d5b7c-113">2</span><span class="sxs-lookup"><span data-stu-id="d5b7c-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="d5b7c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5b7c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b7c-115">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="d5b7c-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



