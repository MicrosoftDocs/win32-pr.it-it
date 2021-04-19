---
title: Risorsa MENU
description: Definisce il contenuto di una risorsa di menu. | Risorsa MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- MENU delle risorse di MENU e altre risorse
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321896"
---
# <a name="menu-resource"></a><span data-ttu-id="24d58-105">Risorsa MENU</span><span class="sxs-lookup"><span data-stu-id="24d58-105">MENU resource</span></span>

<span data-ttu-id="24d58-106">Definisce il contenuto di una risorsa di menu.</span><span class="sxs-lookup"><span data-stu-id="24d58-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="24d58-107">Una risorsa di menu è una raccolta di informazioni che definiscono l'aspetto e la funzione di un menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24d58-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="24d58-108">Un menu è uno strumento di input speciale che consente a un utente di selezionare i comandi e aprire sottomenu da un elenco di voci di menu.</span><span class="sxs-lookup"><span data-stu-id="24d58-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="24d58-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="24d58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d58-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span><span class="sxs-lookup"><span data-stu-id="24d58-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="24d58-111">Numero che identifica il menu.</span><span class="sxs-lookup"><span data-stu-id="24d58-111">Number that identifies the menu.</span></span> <span data-ttu-id="24d58-112">Questo valore è una stringa univoca o un valore Unsigned Integer univoco a 16 bit nell'intervallo compreso tra 1 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="24d58-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="24d58-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="24d58-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="24d58-114">Questo parametro può essere costituito da zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="24d58-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="24d58-115">Istruzione</span><span class="sxs-lookup"><span data-stu-id="24d58-115">Statement</span></span>                                                        | <span data-ttu-id="24d58-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24d58-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24d58-117">[**Caratteristiche**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="24d58-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="24d58-118">Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse.</span><span class="sxs-lookup"><span data-stu-id="24d58-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="24d58-119">Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="24d58-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="24d58-120">[](language-statement.md) *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="24d58-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="24d58-121">Lingua per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="24d58-121">Language for the resource.</span></span> <span data-ttu-id="24d58-122">Per ulteriori informazioni, vedere [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="24d58-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="24d58-123">[](version-statement.md) *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="24d58-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="24d58-124">Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse.</span><span class="sxs-lookup"><span data-stu-id="24d58-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="24d58-125">Per ulteriori informazioni, vedere [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="24d58-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="24d58-126">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="24d58-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="24d58-127">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="24d58-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24d58-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="24d58-128">Examples</span></span>

<span data-ttu-id="24d58-129">Di seguito è riportato un esempio di un'istruzione di **menu** completa:</span><span class="sxs-lookup"><span data-stu-id="24d58-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="24d58-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24d58-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d58-131">Uso di menu</span><span class="sxs-lookup"><span data-stu-id="24d58-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="24d58-132">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="24d58-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="24d58-133">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="24d58-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="24d58-134">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="24d58-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="24d58-135">**MENUEX**</span><span class="sxs-lookup"><span data-stu-id="24d58-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="24d58-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="24d58-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="24d58-137">**POPUP**</span><span class="sxs-lookup"><span data-stu-id="24d58-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="24d58-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="24d58-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="24d58-139">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="24d58-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="24d58-140">**Versione**</span><span class="sxs-lookup"><span data-stu-id="24d58-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
