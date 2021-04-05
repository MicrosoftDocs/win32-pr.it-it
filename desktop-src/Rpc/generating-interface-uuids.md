---
title: Generazione UUID dell'interfaccia
description: Generazione di identificatori univoci universali (UUID) dell'interfaccia e uso di uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710204"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="fa23b-103">Generazione UUID dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="fa23b-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="fa23b-104">Questa sezione presenta informazioni sugli identificatori univoci (UUID) universali e l'utilità uuidgen negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa23b-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="fa23b-105">Che cos'è un UUID?</span><span class="sxs-lookup"><span data-stu-id="fa23b-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="fa23b-106">Uso di uuidgen</span><span class="sxs-lookup"><span data-stu-id="fa23b-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="fa23b-107">Che cos'è un UUID?</span><span class="sxs-lookup"><span data-stu-id="fa23b-107">What is a UUID?</span></span>

<span data-ttu-id="fa23b-108">Tutte le interfacce devono essere identificate in modo univoco in una rete, in modo che i client possano trovarle.</span><span class="sxs-lookup"><span data-stu-id="fa23b-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="fa23b-109">Nelle reti di piccole dimensioni, il nome dell'interfaccia da solo può essere sufficiente per identificarlo.</span><span class="sxs-lookup"><span data-stu-id="fa23b-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="fa23b-110">Tuttavia, ciò non è in genere possibile su reti di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fa23b-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="fa23b-111">Pertanto, gli sviluppatori in genere assegnano a ogni interfaccia un identificatore univoco universale (UUID, interscambiabile con il termine GUID o identificatore univoco globale).</span><span class="sxs-lookup"><span data-stu-id="fa23b-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="fa23b-112">Un UUID è una stringa che contiene un set di cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="fa23b-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="fa23b-113">Ogni interfaccia ha un UUID diverso.</span><span class="sxs-lookup"><span data-stu-id="fa23b-113">Each interface has a different UUID.</span></span> <span data-ttu-id="fa23b-114">Per informazioni dettagliate, vedere [UUID di stringa](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="fa23b-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="fa23b-115">La rappresentazione testuale di un UUID è una stringa costituita da 8 cifre esadecimali seguite da un trattino, seguite da tre gruppi delimitati da trattini di 4 cifre esadecimali, seguite da un trattino, seguite da 12 cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="fa23b-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="fa23b-116">L'esempio seguente è una stringa UUID valida:</span><span class="sxs-lookup"><span data-stu-id="fa23b-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="fa23b-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="fa23b-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="fa23b-118">Gli UUID vuoti sono denominati UUID Nil anziché UUID **null** .</span><span class="sxs-lookup"><span data-stu-id="fa23b-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="fa23b-119">Il termine Nil indica qualsiasi elemento che sia zero, vuoto, vuoto o non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="fa23b-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="fa23b-120">Una stringa vuota, un record di database vuoto o un UUID non inizializzato sono tutti esempi di valori Nil.</span><span class="sxs-lookup"><span data-stu-id="fa23b-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="fa23b-121">Il valore **null** è il valore specifico zero.</span><span class="sxs-lookup"><span data-stu-id="fa23b-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="fa23b-122">Viene spesso usato nella programmazione C e C++ insieme ai puntatori.</span><span class="sxs-lookup"><span data-stu-id="fa23b-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="fa23b-123">Nil è un termine più generico rispetto a **null**.</span><span class="sxs-lookup"><span data-stu-id="fa23b-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="fa23b-124">Gli UUID dell'interfaccia oggetto non inizializzati devono essere sempre definiti UUID Nil anziché UUID **null** .</span><span class="sxs-lookup"><span data-stu-id="fa23b-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="fa23b-125">Uso di uuidgen</span><span class="sxs-lookup"><span data-stu-id="fa23b-125">Using Uuidgen</span></span>

<span data-ttu-id="fa23b-126">Microsoft fornisce un programma di utilità denominato uuidgen per generare gli UUID.</span><span class="sxs-lookup"><span data-stu-id="fa23b-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="fa23b-127">L'utilità uuidgen genera l'UUID nel formato di file IDL o nel formato del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="fa23b-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="fa23b-128">Quando si esegue l'utilità uuidgen dalla riga di comando, è possibile usare le opzioni di comando seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa23b-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="fa23b-129">Opzione uuidgen</span><span class="sxs-lookup"><span data-stu-id="fa23b-129">Uuidgen switch</span></span>           | <span data-ttu-id="fa23b-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa23b-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fa23b-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="fa23b-131">**/I**</span></span>                   | <span data-ttu-id="fa23b-132">Restituisce UUID a un modello di interfaccia IDL.</span><span class="sxs-lookup"><span data-stu-id="fa23b-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="fa23b-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="fa23b-133">**/s**</span></span>                   | <span data-ttu-id="fa23b-134">Restituisce UUID come struttura C inizializzata.</span><span class="sxs-lookup"><span data-stu-id="fa23b-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="fa23b-135">**/o** < *nome file*></span><span class="sxs-lookup"><span data-stu-id="fa23b-135">**/o**<*filename*></span></span> | <span data-ttu-id="fa23b-136">Reindirizza l'output a un file. specificata immediatamente dopo l'opzione **/o** .</span><span class="sxs-lookup"><span data-stu-id="fa23b-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="fa23b-137">**/n** < *numero* di></span><span class="sxs-lookup"><span data-stu-id="fa23b-137">**/n**<*number*></span></span>   | <span data-ttu-id="fa23b-138">Specifica il numero di UUID da generare.</span><span class="sxs-lookup"><span data-stu-id="fa23b-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="fa23b-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="fa23b-139">**/v**</span></span>                   | <span data-ttu-id="fa23b-140">Visualizza le informazioni sulla versione di uuidgen.</span><span class="sxs-lookup"><span data-stu-id="fa23b-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="fa23b-141">**/h** o **?**</span><span class="sxs-lookup"><span data-stu-id="fa23b-141">**/h** or **?**</span></span>          | <span data-ttu-id="fa23b-142">Visualizza il riepilogo delle opzioni di comando.</span><span class="sxs-lookup"><span data-stu-id="fa23b-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="fa23b-143">In genere, si userà l'utilità uuidgen, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="fa23b-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="fa23b-144">**uuidgen-i-oMyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="fa23b-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="fa23b-145">Questo comando genera un UUID e lo archivia in un file MIDL che è possibile usare come modello.</span><span class="sxs-lookup"><span data-stu-id="fa23b-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="fa23b-146">Quando viene eseguito il comando precedente, il contenuto di MyApp. idl è simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="fa23b-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="fa23b-147">Il passaggio successivo consiste nel sostituire il nome del segnaposto, InterfaceName, con il nome effettivo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fa23b-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




