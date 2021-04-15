---
title: Codice di esempio per creare un descrittore di sicurezza
description: Questo argomento include un Visual Basic esempio di codice che illustra come creare un oggetto descrittore di sicurezza per un oggetto ADSI.
ms.assetid: 7c6dcdaf-0bef-4f72-bd9d-dc3ab4295008
ms.tgt_platform: multiple
keywords:
- Codice di esempio per creare un descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dcbe659d8c9b2e639fbd947cc5156807fa09367b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470891"
---
# <a name="example-code-for-creating-a-security-descriptor"></a><span data-ttu-id="34f8f-104">Codice di esempio per creare un descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="34f8f-104">Example Code for Creating a Security Descriptor</span></span>

<span data-ttu-id="34f8f-105">Questo argomento include un Visual Basic esempio di codice che illustra come creare un oggetto descrittore di sicurezza per un oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="34f8f-105">This topic includes a Visual Basic code example that shows you how to create a security descriptor object for an ADSI object.</span></span>


```VB
' This code example assumes that you have the credentials
' required to create objects.
Dim MyObject As IADs
Dim MySecDes As SecurityDescriptor
Dim Var As Variant
Dim SecDes As New SecurityDescriptor
Dim Dacl As New AccessControlList
Dim Ace As New AccessControlEntry

On Error GoTo Cleanup
 
' Create an Access Control Entry (ACE) for Group objects
' at Fabrikam on an LDAP namespace. 
Ace.AccessMask = 0
Ace.AceType = 1
Ace.AceFlags = 1
Ace.Trustee = "cn=Groups,o=Fabrikam"
 
' Add the new ACE object as the only ACE in a new
' access-control list (ACL).
Dacl.AceCount = 1
Dacl.AclRevision = 4
Dacl.AddAce Ace
 
' Use this ACL as the discretionary ACL (DACL) for
' this Security Descriptor object and use this DACL
' instead of the default. 
SecDes.Revision = 1
SecDes.OwnerDefaulted = True
SecDes.GroupDefaulted = True
SecDes.DaclDefaulted = False
SecDes.SaclDefaulted = True
SecDes.DiscretionaryAcl = Dacl

' Attach this security descriptor to the ADSI object.
MyObject.Put "ntSecurityDescriptor", SecDes
' Commit the changes to the underlying directory service.
MyObject.SetInfo
' Read the properties back in to the property cache.
MyObject.GetInfo
' Get the SecurityDescriptor object.
Set MySecDes = MyObject.Get("ntSecurityDescriptor")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyObject = Nothing
    Set MySecDes = Nothing
    Set SecDes = Nothing
    Set Dacl = Nothing
    Set Ace = Nothing
```



 

 




