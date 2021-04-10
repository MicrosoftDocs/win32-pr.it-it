---
title: Codice di esempio per l'impostazione delle autorizzazioni per un gruppo di proprietà
description: Gli esempi di codice C e C++ seguenti creano una voce ACE che assegna l'accesso in lettura e scrittura agli attributi del set di proprietà di informazioni personali degli oggetti utente al trustee specificato.
ms.assetid: 46d53b41-02eb-4830-b625-2d9ffa21a312
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, impostazione delle autorizzazioni per un gruppo di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb45e75aaab9399fc2962b95397380f4bb4eeb3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956328"
---
# <a name="example-code-for-setting-permissions-on-a-group-of-properties"></a><span data-ttu-id="db2a6-104">Codice di esempio per l'impostazione delle autorizzazioni per un gruppo di proprietà</span><span class="sxs-lookup"><span data-stu-id="db2a6-104">Example Code for Setting Permissions on a Group of Properties</span></span>

<span data-ttu-id="db2a6-105">Gli esempi di codice C e C++ seguenti creano una voce ACE che assegna l'accesso in lettura e scrittura agli attributi del set di proprietà di [**informazioni personali**](/windows/desktop/ADSchema/r-personal-information) degli oggetti utente al trustee specificato.</span><span class="sxs-lookup"><span data-stu-id="db2a6-105">The following C and C++ code examples create an ACE that assigns read and write access to the attributes of the [**Personal Information**](/windows/desktop/ADSchema/r-personal-information) property set of user objects to the specified trustee.</span></span>


```C++
/***************************************************************************

    CreateAceChangePersonalInfoPropGroupOfUsers()

    Create an ACE that assigns change (Read/Write) property rights to the 
    attributes of the Personal Information property set for user objects. 
    For this function, the ACE is only inherited; therefore, it is not an 
    effective right on the current object.

***************************************************************************/

HRESULT CreateAceChangePersonalInfoPropGroupOfUsers(LPWSTR pwszTrustee, 
                                                    BOOL fAllowed, 
                                                    IDispatch **ppDispACE)
{
    if(!pwszTrustee || !ppDispACE)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    CComPtr<IADsAccessControlEntry> spACE;
    
    // Create the COM object for the new ACE.
    hr = spACE.CoCreateInstance(CLSID_AccessControlEntry);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set the properties of the new ACE.

    /*
    Set the access mask containing the rights to assign. This function assigns 
    ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP to control change.
    */
    hr = spACE->put_AccessMask(ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set the trustee.
    hr = spACE->put_Trustee(CComBSTR(pwszTrustee));
    if(FAILED(hr))
    {
        return hr;
    }

    // AceType must be ADS_ACETYPE_ACCESS_ALLOWED_OBJECT or ADS_ACETYPE_ACCESS_DENIED_OBJECT.
    if(fAllowed)
    {
        hr = spACE->put_AceType(ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
    }
    else
    {
        hr = spACE->put_AceType(ADS_ACETYPE_ACCESS_DENIED_OBJECT);
    }
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    Set Flags to ADS_FLAG_OBJECT_TYPE_PRESENT | ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT 
    so that the right applies only to a specific property of the specified 
    object class.
    */
    hr = spACE->put_Flags(ADS_FLAG_OBJECT_TYPE_PRESENT | ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set ObjectType to the rightsGUID of the Personal Information controlAccessRight object. 
    hr = spACE->put_ObjectType(CComBSTR("{77B5B886-944A-11d1-AEBD-0000F80367C1}"));
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    For this function, set AceFlags so that ACE is inherited by child objects, 
    but not effective on the current object. Set AceFlags to ADS_ACEFLAG_INHERIT_ACE 
    and ADS_ACEFLAG_INHERIT_ONLY_ACE.
    */
    hr = spACE->put_AceFlags(ADS_ACEFLAG_INHERIT_ACE | ADS_ACEFLAG_INHERIT_ONLY_ACE);
    if(FAILED(hr))
    {
        return hr;
    }

    // Set InheritedObjectType to schemaIDGUID of the user class.
    hr = spACE->put_InheritedObjectType(CComBSTR("{BF967ABA-0DE6-11D0-A285-00AA003049E2}"));
    if(FAILED(hr))
    {
        return hr;
    }

    // Call the QueryInterface method for the IDispatch pointer to pass to the AddAce method.
    hr = spACE->QueryInterface(IID_IDispatch, (void**)ppDispACE);
    if(FAILED(hr))
    {
        return hr;
    }

    return hr;
}
```



 

 