---
description: Se si tenta di rimuovere più di un elemento in una raccolta, è possibile che alcuni elementi non siano stati rimossi.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Rimozione di più elementi da una raccolta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17795378f5215977e5e7c2d0afd745c5d02fe6b294d062fcdbcf82f7ccc15351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992441"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Rimozione di più elementi da una raccolta WMI

Se si tenta di rimuovere più di un elemento in una raccolta, è possibile che alcuni elementi non siano stati rimossi. Non è possibile eseguire l'iterazione di una raccolta durante la rimozione di elementi, perché quando si rimuove un elemento da una raccolta, il puntatore alla raccolta viene spostato sull'elemento successivo. Ad esempio, un tentativo di rimuovere tutti gli elementi da una raccolta comporta la rimozione di tutti gli altri elementi. Questo problema può verificarsi quando si rimuovono elementi con i metodi [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) o [**SWbemPropertySet.Remove.**](swbempropertyset-remove.md) È possibile evitare questo problema scorrendo la raccolta e inserendo i nomi degli elementi da rimuovere in una matrice. È quindi possibile scorrere la matrice ed eliminare gli elementi denominati nella matrice. Anche le raccolte, ad esempio [**SWbemNamedValueSet,**](swbemnamedvalueset.md) [**SWbemPrivilegeSet**](swbemprivilegeset.md)e [**SWbemRefresher,**](swbemrefresher.md)hanno un metodo che elimina tutti gli elementi nel contenitore di aggiornamento.

Lo script seguente illustra come rimuovere diversi elementi da una raccolta.


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



Non è possibile rimuovere proprietà e qualificatori in un'istanza di classe o in una classe derivata con proprietà ereditate. Un tentativo di eliminazione di questo tipo genera un errore e la proprietà o il qualificatore non viene rimosso. WMI reimposta invece la proprietà o il qualificatore sul valore predefinito. Nel caso di una classe derivata con proprietà ereditate, WMI reimposta la proprietà ereditata sul valore predefinito della proprietà nella classe padre.

Per altre informazioni, vedere Modifica di informazioni su classi e [istanze,](manipulating-class-and-instance-information.md)Accesso [a](accessing-a-collection.md)una raccolta e Rimozione di un singolo [elemento da una raccolta.](removing-a-single-item-from-a-collection.md)

 

 



