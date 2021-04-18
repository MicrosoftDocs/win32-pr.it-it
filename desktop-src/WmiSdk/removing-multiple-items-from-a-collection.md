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
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Rimozione di più elementi da una raccolta WMI

Se si tenta di rimuovere più di un elemento in una raccolta, è possibile notare che alcuni elementi non vengono rimossi. Non è possibile eseguire l'iterazione di una raccolta durante la rimozione degli elementi, perché quando si rimuove un elemento da una raccolta, il puntatore della raccolta viene spostato all'elemento successivo. Ad esempio, un tentativo di rimuovere tutti gli elementi da una raccolta comporta la rimozione di tutti gli altri elementi. Questo problema può essere visualizzato quando si rimuovono elementi con i metodi [**dell'SWbemQualifierSet. Remove**](swbemqualifierset-remove.md) o [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) . Per evitare questo problema, è possibile scorrere la raccolta e inserire i nomi degli elementi da rimuovere in una matrice. È quindi possibile scorrere la matrice ed eliminare gli elementi denominati nella matrice. Le raccolte, ad esempio [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)e [**SWbemRefresher**](swbemrefresher.md), hanno anche un metodo che elimina tutti gli elementi nel contenitore di aggiornamento.

Nello script seguente viene illustrato come rimuovere diversi elementi da una raccolta.


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



Non è possibile rimuovere proprietà e qualificatori in un'istanza di classe o in una classe derivata che ha proprietà ereditate. Un tentativo di eliminazione di questo tipo genera un errore e la proprietà o il qualificatore non viene rimosso. al contrario, WMI Reimposta la proprietà o il qualificatore sul valore predefinito. Nel caso di una classe derivata con proprietà ereditate, WMI Reimposta la proprietà ereditata sul valore predefinito della proprietà nella classe padre.

Per ulteriori informazioni, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md), [accesso a una raccolta](accessing-a-collection.md)e [rimozione di un singolo elemento da una raccolta](removing-a-single-item-from-a-collection.md).

 

 



