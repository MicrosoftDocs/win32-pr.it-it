---
title: Codice di esempio per la creazione di un oggetto crossRef esterno
description: Questo argomento include un esempio di codice che crea un oggetto crossRef esterno.
ms.assetid: 282ca648-3bc7-4c5b-98db-1d8f2d040e3a
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, creazione di un oggetto crossRef esterno
- Esempi di Active Directory Active Directory creazione di un ad di riferimento esterno , codice di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19b3ee6eb9f13171576cac1a0c656139cee83b7a689eadcb89a33f2807eb8b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190754"
---
# <a name="example-code-for-creating-an-external-crossref-object"></a>Codice di esempio per la creazione di un oggetto crossRef esterno

Nell'Visual Basic di codice seguente viene illustrato come creare un [**oggetto crossRef**](/windows/desktop/ADSchema/c-crossref) esterno.


```VB
' CreateCrossRef()
'
' Description: Creates a crossRef object in the partitions container.
'
' Parameters:
'
' CrossRefName - Contains the name of the crossRef object.
'
' CrossRefDNSRoot - Contains the value to be set for the dNSRoot
' attribute of the crossRef object.
'
' CrossRefNCName - Contains the value to be set for the nCName 
' attribute of the crossRef object.
'

Sub CreateCrossRef(CrossRefName, _
                    CrossRefDNSRoot, _
                    CrossRefNCName)
    Dim oRootDSE As IADs
    Dim oPartitions As IADsContainer
    Dim ADsPath As String
    Dim oCrossRef As IADs

    ' Get the configurationNamingContext property from the 
    ' RootDSE object.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    ADsPath = "LDAP://CN=Partitions," + 
              oRootDSE.Get("configurationNamingContext")
    
    ' Bind to the Partitions container.
    Set oPartitions = GetObject(ADsPath)
    
    ' Create the crossRef object.
    Set oCrossRef = oPartitions.Create("crossRef", 
                                       "CN=" & CrossRefName)
    
    ' Set the dNSRoot attribute.
    oCrossRef.Put "dNSRoot", CrossRefDNSRoot
    
    ' Set the nCName attribute.
    oCrossRef.Put "nCName", CrossRefNCName
    
    ' Commit the crossRef object to the directory.
    oCrossRef.SetInfo
End Sub
```



 

 