---
description: ICE04 verifica che il numero di sequenza di ogni file nella tabella file sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della tabella media.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967797"
---
# <a name="ice04"></a><span data-ttu-id="46abf-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="46abf-103">ICE04</span></span>

<span data-ttu-id="46abf-104">ICE04 verifica che il numero di sequenza di ogni file nella [tabella file](file-table.md) sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della [tabella media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="46abf-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="46abf-105">Ogni record della tabella multimediale rappresenta un disco del supporto di origine contenente tutti i file con un numero di sequenza minore o uguale al valore nella colonna LastSequence e maggiore del valore di LastSequence nel record del disco precedente.</span><span class="sxs-lookup"><span data-stu-id="46abf-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="46abf-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="46abf-106">Result</span></span>

<span data-ttu-id="46abf-107">ICE04 Invia un messaggio di errore se è presente un file con un numero di sequenza maggiore del numero di LastSequence più grande per il supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="46abf-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="46abf-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="46abf-108">Example</span></span>

<span data-ttu-id="46abf-109">ICE04 segnala l'errore seguente per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="46abf-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="46abf-110">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="46abf-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="46abf-111">File</span><span class="sxs-lookup"><span data-stu-id="46abf-111">File</span></span>   | <span data-ttu-id="46abf-112">Sequenza</span><span class="sxs-lookup"><span data-stu-id="46abf-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="46abf-113">MyFile</span><span class="sxs-lookup"><span data-stu-id="46abf-113">MyFile</span></span> | <span data-ttu-id="46abf-114">210</span><span class="sxs-lookup"><span data-stu-id="46abf-114">210</span></span>      |



 

<span data-ttu-id="46abf-115">[Tabella media](media-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="46abf-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="46abf-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="46abf-116">DiskId</span></span> | <span data-ttu-id="46abf-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="46abf-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="46abf-118">1</span><span class="sxs-lookup"><span data-stu-id="46abf-118">1</span></span>      | <span data-ttu-id="46abf-119">100</span><span class="sxs-lookup"><span data-stu-id="46abf-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="46abf-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46abf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46abf-121">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="46abf-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



