---
description: Uno degli scopi principali dell'accesso a una raccolta è rimuovere un elemento dalla raccolta. È possibile rimuovere un elemento da una raccolta con una chiamata al metodo SWbemPropertySet.Remove. Questo metodo non è disponibile per SWbemObjectSet o SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Rimozione di un singolo elemento da una raccolta WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50364173aff9f28362878e84d5f3ddb496e430521dc5b1bb92bbc11e7e6b528c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995901"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Rimozione di un singolo elemento da una raccolta WMI

Uno degli scopi principali dell'accesso a una raccolta è rimuovere un elemento dalla raccolta. È possibile rimuovere un elemento da una raccolta con una chiamata al [**metodo SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Questo metodo non è disponibile per [**SWbemObjectSet**](swbemobjectset.md) o [**SWbemMethodSet.**](swbemmethodset.md)

Gli elementi vengono rimossi in base al nome [**da SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemNamedValueSet**](swbemnamedvalueset.md). Tuttavia, gli elementi in [**SWbemRefresher**](swbemrefresher.md) vengono rimossi per indice e da [**SWbemPrivilegeSet**](swbemprivilegeset.md) dalla costante che rappresenta il nome del privilegio.

**Per rimuovere un elemento da una raccolta**

-   Nell'esempio di codice seguente viene illustrato come rimuovere l'elemento con una chiamata al [**metodo SWbemPropertySet.Remove.**](swbempropertyset-remove.md)

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    L'esempio seguente crea una nuova classe denominata "NewClass" nello spazio dei nomi radice predefinito \\ e aggiunge tre proprietà. Lo script usa quindi il codice dell'esempio precedente per eliminare la seconda proprietà.

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

    

Per altre informazioni, vedere Modifica di informazioni su classi e [istanze,](manipulating-class-and-instance-information.md)Accesso [a una raccolta](accessing-a-collection.md)e Rimozione di più elementi da una [raccolta.](removing-multiple-items-from-a-collection.md)

 

 



