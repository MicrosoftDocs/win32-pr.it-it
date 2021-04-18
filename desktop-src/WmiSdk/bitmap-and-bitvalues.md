---
description: È un numero intero collegato a una proprietà con i qualificatori di BitMap e BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificatori BitMap e BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310415"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="b1e48-103">Qualificatori BitMap e BitValue</span><span class="sxs-lookup"><span data-stu-id="b1e48-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="b1e48-104">Una bitmap è un numero intero collegato a una proprietà con i qualificatori di **bitmap** e **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="b1e48-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="b1e48-105">Ogni bit del valore della proprietà funge da indice nella matrice di valori nell'elenco di **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="b1e48-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="b1e48-106">Poiché più bit nel valore della proprietà possono essere contemporaneamente "on", è possibile usare un singolo valore di proprietà per indicare più valori simultanei.</span><span class="sxs-lookup"><span data-stu-id="b1e48-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="b1e48-107">Ad esempio, l'esempio di codice MOF seguente stabilisce la proprietà **FileType** con i qualificatori **bitmap** e **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="b1e48-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="b1e48-108">Stabilisce inoltre che il bit di ordine inferiore (bit 0) corrisponde al valore di "sola lettura".</span><span class="sxs-lookup"><span data-stu-id="b1e48-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="b1e48-109">Il bit successivo (bit 1) corrisponde a "hidden" e così via.</span><span class="sxs-lookup"><span data-stu-id="b1e48-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="b1e48-110">(Non tutti i bit devono essere significativi.</span><span class="sxs-lookup"><span data-stu-id="b1e48-110">(Not all bits must be significant.</span></span> <span data-ttu-id="b1e48-111">In questo sistema a otto bit, i due bit di ordine superiore, 6 e 7, non hanno alcun significato.</span><span class="sxs-lookup"><span data-stu-id="b1e48-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="b1e48-112">Se la proprietà **FileType** riporta il valore 7 (BITS 0000 0111), il file è di sola lettura, "System" e "hidden".</span><span class="sxs-lookup"><span data-stu-id="b1e48-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="b1e48-113">Se la proprietà **FileType** riporta il valore 18 (0x12, BITS 0001 0010), si tratta di una sottodirectory nascosta.</span><span class="sxs-lookup"><span data-stu-id="b1e48-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="b1e48-114">Esistono due tipi diversi di bitmap che usano il codice MOF:</span><span class="sxs-lookup"><span data-stu-id="b1e48-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="b1e48-115">Bit significativi consecutivi che iniziano con il bit di ordine inferiore (bit 0)</span><span class="sxs-lookup"><span data-stu-id="b1e48-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="b1e48-116">È possibile definire una matrice di valori di bit senza specificare in modo esplicito i bit significativi se i bit significativi iniziano con il bit di ordine inferiore (bit 0) e avanzare verso l'alto senza interruzioni in tutti gli elementi della matrice **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="b1e48-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="b1e48-117">Nell'esempio di codice MOF seguente viene eseguita la stessa funzione dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="b1e48-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="b1e48-118">Bit significativo preceduto da un bit non significativo</span><span class="sxs-lookup"><span data-stu-id="b1e48-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="b1e48-119">Se il bit di ordine inferiore non è significativo o la sequenza di bit significativi non è continua, è necessario specificare sia la **bitmap** che i qualificatori **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="b1e48-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="b1e48-120">Nell'esempio di codice MOF riportato di seguito viene illustrata una situazione in cui il bit di ordine inferiore non è significativo e si verifica un gap nella sequenza di bit significativi.</span><span class="sxs-lookup"><span data-stu-id="b1e48-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="b1e48-121">In questo caso, l'impostazione del bit di ordine inferiore (bit 0) non ha significato e viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b1e48-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="b1e48-122">Tuttavia, l'impostazione del bit 1 (0x2) indica che questo messaggio di posta elettronica è contrassegnato per il completamento, l'impostazione del bit 4 (0x8) indica che una ricevuta di recapito deve essere inviata al mittente quando il messaggio di posta elettronica è arrivato alla cassetta postale del destinatario e l'impostazione del bit 5 (0x10) specifica che una ricevuta di lettura deve essere inviata al mittente quando il messaggio di</span><span class="sxs-lookup"><span data-stu-id="b1e48-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="b1e48-123">Impostando tutti e tre i bit significativi (0x1A) si specificano tutte e tre le condizioni per il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b1e48-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e48-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1e48-124">Remarks</span></span>

<span data-ttu-id="b1e48-125">Per decidere se utilizzare i qualificatori dei valori di **bitmap** / **BitValues** o **ValueMap** /  , determinare se i valori indicati possono verificarsi simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="b1e48-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="b1e48-126">Se possono esistere più valori simultanei, è necessario utilizzare la **bitmap** / **BitValues**.</span><span class="sxs-lookup"><span data-stu-id="b1e48-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="b1e48-127">Se tutti i valori si escludono a vicenda, è necessario usare i / qualificatori dei **valori** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="b1e48-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1e48-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1e48-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e48-129">Qualificatori ValueMap e value</span><span class="sxs-lookup"><span data-stu-id="b1e48-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



