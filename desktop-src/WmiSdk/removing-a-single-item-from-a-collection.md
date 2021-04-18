---
description: Uno degli scopi principali per accedere a una raccolta consiste nel rimuovere un elemento dalla raccolta. È possibile rimuovere un elemento da una raccolta con una chiamata al metodo SWbemPropertySet. Remove. Questo metodo non è disponibile per SWbemObjectSet o SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Rimozione di un singolo elemento da una raccolta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309910"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="0a37e-105">Rimozione di un singolo elemento da una raccolta WMI</span><span class="sxs-lookup"><span data-stu-id="0a37e-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="0a37e-106">Uno degli scopi principali per accedere a una raccolta consiste nel rimuovere un elemento dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="0a37e-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="0a37e-107">È possibile rimuovere un elemento da una raccolta con una chiamata al metodo [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="0a37e-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="0a37e-108">Questo metodo non è disponibile per [**SWbemObjectSet**](swbemobjectset.md) o [**SWbemMethodSet**](swbemmethodset.md).</span><span class="sxs-lookup"><span data-stu-id="0a37e-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="0a37e-109">Gli elementi vengono rimossi in base al nome da [**SWbemPropertySet**](swbempropertyset.md), [**dell'SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span><span class="sxs-lookup"><span data-stu-id="0a37e-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="0a37e-110">Tuttavia, gli elementi in [**SWbemRefresher**](swbemrefresher.md) vengono rimossi dall'indice e da [**SWbemPrivilegeSet**](swbemprivilegeset.md) dalla costante che rappresenta il nome del privilegio.</span><span class="sxs-lookup"><span data-stu-id="0a37e-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="0a37e-111">**Per rimuovere un elemento da una raccolta**</span><span class="sxs-lookup"><span data-stu-id="0a37e-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="0a37e-112">Nell'esempio di codice seguente viene illustrato come rimuovere l'elemento con una chiamata al metodo [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="0a37e-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="0a37e-113">Nell'esempio seguente viene creata una nuova classe denominata "NewClass" nello \\ spazio dei nomi predefinito radice a cui vengono aggiunte tre proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a37e-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="0a37e-114">Lo script usa quindi il codice dell'esempio precedente per eliminare la seconda proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a37e-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="0a37e-115">Per ulteriori informazioni, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md), [accesso a una raccolta](accessing-a-collection.md)e [rimozione di più elementi da una raccolta](removing-multiple-items-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="0a37e-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



