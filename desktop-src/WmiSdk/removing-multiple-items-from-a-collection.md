---
description: Se si tenta di rimuovere più di un elemento in una raccolta, è possibile notare che alcuni elementi non vengono rimossi.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Rimozione di più elementi da una raccolta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318539"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="762bc-103">Rimozione di più elementi da una raccolta WMI</span><span class="sxs-lookup"><span data-stu-id="762bc-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="762bc-104">Se si tenta di rimuovere più di un elemento in una raccolta, è possibile notare che alcuni elementi non vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="762bc-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="762bc-105">Non è possibile eseguire l'iterazione di una raccolta durante la rimozione degli elementi, perché quando si rimuove un elemento da una raccolta, il puntatore della raccolta viene spostato all'elemento successivo.</span><span class="sxs-lookup"><span data-stu-id="762bc-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="762bc-106">Ad esempio, un tentativo di rimuovere tutti gli elementi da una raccolta comporta la rimozione di tutti gli altri elementi.</span><span class="sxs-lookup"><span data-stu-id="762bc-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="762bc-107">Questo problema può essere visualizzato quando si rimuovono elementi con i metodi [**dell'SWbemQualifierSet. Remove**](swbemqualifierset-remove.md) o [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="762bc-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="762bc-108">Per evitare questo problema, è possibile scorrere la raccolta e inserire i nomi degli elementi da rimuovere in una matrice.</span><span class="sxs-lookup"><span data-stu-id="762bc-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="762bc-109">È quindi possibile scorrere la matrice ed eliminare gli elementi denominati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="762bc-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="762bc-110">Le raccolte, ad esempio [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)e [**SWbemRefresher**](swbemrefresher.md), hanno anche un metodo che elimina tutti gli elementi nel contenitore di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="762bc-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="762bc-111">Nello script seguente viene illustrato come rimuovere diversi elementi da una raccolta.</span><span class="sxs-lookup"><span data-stu-id="762bc-111">The following script illustrates how to remove several items from a collection.</span></span>


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



Non è possibile rimuovere proprietà e qualificatori in un'istanza di classe o in una classe derivata che ha proprietà ereditate. Un tentativo di eliminazione di questo tipo genera un errore e la proprietà o il qualificatore non viene rimosso. al contrario, WMI Reimposta la proprietà o il qualificatore sul valore predefinito. <span data-ttu-id="762bc-114">Nel caso di una classe derivata con proprietà ereditate, WMI Reimposta la proprietà ereditata sul valore predefinito della proprietà nella classe padre.</span><span class="sxs-lookup"><span data-stu-id="762bc-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="762bc-115">Per ulteriori informazioni, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md), [accesso a una raccolta](accessing-a-collection.md)e [rimozione di un singolo elemento da una raccolta](removing-a-single-item-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="762bc-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 



