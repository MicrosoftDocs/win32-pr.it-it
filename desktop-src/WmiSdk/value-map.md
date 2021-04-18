---
description: Una mappa di valori è una matrice collegata a una proprietà con il valore e i qualificatori ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Qualificatori ValueMap e value
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315184"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="3a66f-103">Qualificatori ValueMap e value</span><span class="sxs-lookup"><span data-stu-id="3a66f-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="3a66f-104">Una mappa di valori è una matrice collegata a una proprietà con il **valore** e i qualificatori **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="3a66f-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="3a66f-105">La proprietà funge da indice nella matrice, mantenendo un valore che rappresenta uno dei valori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3a66f-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="3a66f-106">Utilizzando il codice MOF, è possibile disporre dei seguenti tipi di mappe dei valori:</span><span class="sxs-lookup"><span data-stu-id="3a66f-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="3a66f-107">Mapping della matrice a un intero.</span><span class="sxs-lookup"><span data-stu-id="3a66f-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="3a66f-108">È possibile definire una matrice con il qualificatore del **valore** e collegare la matrice direttamente a una proprietà Integer, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="3a66f-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="3a66f-109">In questo esempio il valore della proprietà **status** è un indice nella matrice di stringhe definita per **valore**.</span><span class="sxs-lookup"><span data-stu-id="3a66f-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="3a66f-110">La proprietà può assumere solo valori che corrispondono alle posizioni ordinali nella matrice di **valori** meno 1.</span><span class="sxs-lookup"><span data-stu-id="3a66f-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="3a66f-111">Ad esempio, se si imposta **status** su "1" viene eseguito il mapping al valore "Error".</span><span class="sxs-lookup"><span data-stu-id="3a66f-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="3a66f-112">La proprietà index può assumere solo valori che corrispondono alle posizioni nella matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="3a66f-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="3a66f-113">Se, ad esempio, la matrice contiene 10 voci, la proprietà index può essere storia da 0 a 9, non 30 o 177.</span><span class="sxs-lookup"><span data-stu-id="3a66f-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="3a66f-114">Mapping della matrice a un altro mapping della matrice a un intero.</span><span class="sxs-lookup"><span data-stu-id="3a66f-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="3a66f-115">Se si desidera creare un indice che non utilizza un sistema ordinale di conteggio, utilizzare il qualificatore **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="3a66f-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="3a66f-116">Il qualificatore **ValueMap** configura un'altra matrice che contiene un sistema di numerazione degli indici arbitrari, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="3a66f-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="3a66f-117">Sebbene sia necessario inserire i valori di **ValueMap** in Quotations, WMI considera i valori integer.</span><span class="sxs-lookup"><span data-stu-id="3a66f-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="3a66f-118">Pertanto, in questo esempio è possibile impostare la proprietà **status** su un valore integer nel set di **ValueMap** : 1, 3, 99 o 0.</span><span class="sxs-lookup"><span data-stu-id="3a66f-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="3a66f-119">WMI esegue il mapping di ogni intero da una posizione ordinale nella matrice di stringhe **ValueMap** a una posizione corrispondente nella matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="3a66f-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="3a66f-120">Ad esempio, l'impostazione **dello stato** su 0 corrisponde a "Unknown".</span><span class="sxs-lookup"><span data-stu-id="3a66f-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="3a66f-121">Mapping della matrice a un altro mapping della matrice a una stringa.</span><span class="sxs-lookup"><span data-stu-id="3a66f-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="3a66f-122">Se non si vuole usare un numero intero per indicizzare la matrice, è possibile usare invece una stringa per includere uno dei valori possibili nella matrice.</span><span class="sxs-lookup"><span data-stu-id="3a66f-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="3a66f-123">A tale scopo, è necessario definire sia un **valore** sia una matrice **ValueMap** che contengono entrambe stringhe, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="3a66f-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="3a66f-124">Con una proprietà stringa, i valori effettivi consentiti della proprietà sono le voci nella matrice **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="3a66f-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="3a66f-125">Ad esempio, è possibile impostare **lo stato** su "OK" o "sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="3a66f-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="3a66f-126">L'applicazione può sfruttare i vantaggi dei mapping in modo utile.</span><span class="sxs-lookup"><span data-stu-id="3a66f-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="3a66f-127">Il provider deve applicare un intervallo di valori valido.</span><span class="sxs-lookup"><span data-stu-id="3a66f-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a66f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a66f-128">Remarks</span></span>

<span data-ttu-id="3a66f-129">Per decidere se utilizzare il valore **ValueMap** /  o i  / qualificatori di bitmap **BitValues** , determinare se uno dei valori indicati potrebbe verificarsi simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="3a66f-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="3a66f-130">Se possono esistere più valori simultanei, è necessario utilizzare la **bitmap** / **BitValues**.</span><span class="sxs-lookup"><span data-stu-id="3a66f-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="3a66f-131">Se tutti i valori si escludono a vicenda, è necessario usare i / qualificatori di **valore** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="3a66f-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a66f-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a66f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a66f-133">BitMap e BitValue</span><span class="sxs-lookup"><span data-stu-id="3a66f-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



