---
title: Codice di esempio per l'impostazione dei diritti per tipi specifici di oggetti
description: Nell'esempio di codice C/C++ riportato di seguito viene creata una voce ACE che assegna i diritti ereditati dal tipo specificato di oggetto, ma che non sono validi per l'oggetto corrente.
ms.assetid: c36ae0c8-40ad-4afd-8552-4de77f4463e2
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, impostazione dei diritti per tipi specifici di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff598c8db6a48e07f48a3e846f54b75b2d39255
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707633"
---
# <a name="example-code-for-setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="5419e-104">Codice di esempio per l'impostazione dei diritti per tipi specifici di oggetti</span><span class="sxs-lookup"><span data-stu-id="5419e-104">Example Code for Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="5419e-105">Nell'esempio di codice C/C++ riportato di seguito viene creata una voce ACE che assegna i diritti ereditati dal tipo specificato di oggetto, ma che non sono validi per l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="5419e-105">The following C/C++ code example creates an ACE that assigns rights that are inherited by the specified type of object, but are not effective on the current object.</span></span>


```C++
// Create an ACE that is inherited by child objects of the specified type,
// but does not apply to the current object.
// This ACE is also propagated to all descendants of the current object.
HRESULT CreateAceNoEffectiveInheritObject(
    LPWSTR pwszTrustee,
    long lAccessRights,
    long lAccessType,
    LPWSTR pwszObjectGUID,
    LPWSTR pwszInheritedObjectGUID,
    IDispatch **ppDispACE)
{
    
    HRESULT hr = E_FAIL;
    IADsAccessControlEntry *pACE = NULL;
    long lFlags = 0L;
    
    // Create the COM object for the new ACE.
    hr  = CoCreateInstance( CLSID_AccessControlEntry,
                            NULL,
                            CLSCTX_INPROC_SERVER,
                            IID_IADsAccessControlEntry,
                            (void **)&pACE);
    if (SUCCEEDED(hr))
    {
        // Set the properties of the new ACE.
        
        // Set the access mask that contains the rights to assign.
        hr = pACE->put_AccessMask(lAccessRights);

        // Set the trustee.
        hr = pACE->put_Trustee(pwszTrustee);
        
        // Set the AceType.
        hr = pACE->put_AceType(lAccessType);
        
        /*
        For this function, set AceFlags so that ACE is inherited by child 
        objects, but not effective on the current object.
        */
        
        // Set AceFlags to ADS_ACEFLAG_INHERIT_ACE and ADS_ACEFLAG_INHERIT_ONLY_ACE.
        hr = pACE->put_AceFlags(ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE);
        
        /*
        If an szObjectGUID is specified, add ADS_FLAG_OBJECT_TYPE_PRESENT flag 
        to the lFlags mask and set the ObjectType.
        */
        if (pwszObjectGUID)
        {
            lFlags |= ADS_FLAG_OBJECT_TYPE_PRESENT;
            hr = pACE->put_ObjectType(pwszObjectGUID);
        }
        
        /*
        If an szInheritedObjectGUID is specified, add 
        ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT flag to the lFlags mask and set 
        the InheritedObjectType.
        */
        if (pwszInheritedObjectGUID)
        {
            lFlags |= ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT;
            hr = pACE->put_InheritedObjectType(pwszInheritedObjectGUID);
        }
        
        // Set flags if ObjectType or InheritedObjectType were set.
        if (lFlags)
        {
            hr = pACE->put_Flags(lFlags);
        }
        
        // QueryInterface for a IDispatch pointer to pass to the AddAce method.
        hr = pACE->QueryInterface(IID_IDispatch, (void**)ppDispACE);
    }
     
    return hr;
}
```



 

 




