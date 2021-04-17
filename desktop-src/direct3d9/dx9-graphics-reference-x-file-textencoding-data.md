---
description: Gli oggetti dati contengono i dati effettivi o un riferimento a tali dati. Ogni oggetto dati dispone di un modello corrispondente che specifica il tipo di dati. Nelle sezioni seguenti vengono illustrati il form e le parti degli oggetti dati.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Data (formato file X, codifica testo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401248"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="21b11-105">Data (formato file X, codifica testo)</span><span class="sxs-lookup"><span data-stu-id="21b11-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="21b11-106">Gli oggetti dati contengono i dati effettivi o un riferimento a tali dati.</span><span class="sxs-lookup"><span data-stu-id="21b11-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="21b11-107">Ogni oggetto dati dispone di un modello corrispondente che specifica il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="21b11-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="21b11-108">Nelle sezioni seguenti vengono illustrati il form e le parti degli oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="21b11-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="21b11-109">Form, identificatore e nome</span><span class="sxs-lookup"><span data-stu-id="21b11-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="21b11-110">Gli oggetti dati hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="21b11-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="21b11-111">L'identificatore è obbligatorio e deve corrispondere a una primitiva o a un tipo di dati definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="21b11-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="21b11-112">Il nome è tuttavia facoltativo.</span><span class="sxs-lookup"><span data-stu-id="21b11-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="21b11-113">Membri dei dati</span><span class="sxs-lookup"><span data-stu-id="21b11-113">Data Members</span></span>

<span data-ttu-id="21b11-114">I membri dati possono essere uno dei seguenti: oggetto dati, riferimento ai dati, elenco di numeri interi, elenco float o elenco stringhe.</span><span class="sxs-lookup"><span data-stu-id="21b11-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="21b11-115">Un oggetto dati è un oggetto dati annidato.</span><span class="sxs-lookup"><span data-stu-id="21b11-115">A data object is a nested data object.</span></span> <span data-ttu-id="21b11-116">Ciò consente di esprimere la natura gerarchica del formato di file.</span><span class="sxs-lookup"><span data-stu-id="21b11-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="21b11-117">I tipi di oggetti dati annidati consentiti nella gerarchia possono essere limitati.</span><span class="sxs-lookup"><span data-stu-id="21b11-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="21b11-118">Un riferimento ai dati è un riferimento a un oggetto dati precedentemente rilevato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="21b11-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="21b11-119">Un elenco di numeri interi è un elenco di numeri interi separato da punti e virgola, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="21b11-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="21b11-120">Un elenco float è un elenco delimitato da punti e virgola di float, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="21b11-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="21b11-121">Un elenco di stringhe è un elenco di stringhe delimitato da punto e virgola, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="21b11-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="21b11-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21b11-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21b11-123">Codifica testo</span><span class="sxs-lookup"><span data-stu-id="21b11-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



