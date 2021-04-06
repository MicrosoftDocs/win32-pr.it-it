---
title: Codice di esempio per la verifica dell'accesso a un controllo a destra nell'ACL di un oggetto
description: L'esempio seguente può essere usato per verificare che l'utente attualmente connesso disponga delle autorizzazioni per un controllo di accesso Right sull'oggetto specificato.
ms.assetid: 360320b8-32bd-4141-924b-25833a2761c8
ms.tgt_platform: multiple
keywords:
- Codice di esempio per la verifica dell'accesso a un controllo a destra nell'ACL di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b95054a7f21f1b9e96a7e6e0b723718598e8012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855453"
---
# <a name="example-code-for-checking-a-control-access-right-in-an-objects-acl"></a>Codice di esempio per la verifica dell'accesso a un controllo a destra nell'ACL di un oggetto

L'esempio seguente può essere usato per verificare che l'utente attualmente connesso disponga delle autorizzazioni per un controllo di accesso Right sull'oggetto specificato.


```C++
// Define the Generic Mapping structure.
// Generic read
#define GENERIC_READ_MAPPING     ((STANDARD_RIGHTS_READ)     | \
                                  (ADS_RIGHT_ACTRL_DS_LIST)   | \
                                  (ADS_RIGHT_DS_READ_PROP)   | \
                                  (ADS_RIGHT_DS_LIST_OBJECT))
// Generic execute
#define GENERIC_EXECUTE_MAPPING  ((STANDARD_RIGHTS_EXECUTE)  | \
                                  (ADS_RIGHT_ACTRL_DS_LIST))
// Generic right
#define GENERIC_WRITE_MAPPING    ((STANDARD_RIGHTS_WRITE)    | \
                                  (ADS_RIGHT_DS_SELF)      | \
                  (ADS_RIGHT_DS_WRITE_PROP))
// Generic all
#define GENERIC_ALL_MAPPING      ((STANDARD_RIGHTS_REQUIRED) | \
                                  (ADS_RIGHT_DS_CREATE_CHILD)    | \
                                  (ADS_RIGHT_DS_DELETE_CHILD)    | \
                                  (ADS_RIGHT_DS_DELETE_TREE)     | \
                                  (ADS_RIGHT_DS_READ_PROP)   | \
                                  (ADS_RIGHT_DS_WRITE_PROP)  | \
                                  (ADS_RIGHT_ACTRL_DS_LIST)   | \
                                  (ADS_RIGHT_DS_LIST_OBJECT)     | \
                                  (ADS_RIGHT_DS_CONTROL_ACCESS)  | \
                                  (ADS_RIGHT_DS_SELF))
// Standard DS generic access rights mapping
#define DS_GENERIC_MAPPING {GENERIC_READ_MAPPING,    \
                GENERIC_WRITE_MAPPING,   \
                GENERIC_EXECUTE_MAPPING, \
                GENERIC_ALL_MAPPING}
 
HRESULT CheckExtendedRight(
                            HANDLE hToken,
                            IDirectoryObject *pObject,
                            CLSID pclsid,
                            DWORD *dwAccess
                            )
 
{
HRESULT hr = E_FAIL;
*dwAccess = FALSE;
BOOL bSuccess = FALSE;
PADS_ATTR_INFO pAttrInfo = NULL;
DWORD   dwReturn= 0;
LPWSTR   pAttrNames[]= {L"nTSecurityDescriptor",L"objectSid"};
PSECURITY_DESCRIPTOR pSD = NULL;
DWORD   SDSize;
VOID    *pAbsoluteSD = NULL; 
DWORD   AbsoluteSDSize = 0;
VOID    *pDacl = NULL;
DWORD   DaclSize = 0;
VOID    *pSacl = NULL;
DWORD   SaclSize = 0;
VOID    *pOwner = NULL;
DWORD   OwnerSize = 0;
VOID    *pGroup = NULL;
DWORD   GroupSize = 0;
PSID pSID = NULL;
UINT nGUIDLength = 0;

// Get attributes for security descriptor and SID.
hr = pObject->GetObjectAttributes( pAttrNames, 
                                  2, 
                                  &pAttrInfo, 
                                  &dwReturn );
if ( (SUCCEEDED(hr)) && (dwReturn>0) )
{
    for(DWORD idx=0; idx < dwReturn;idx++, pAttrInfo++ )
    {
        // Verify the attribute name.
        if ( _wcsicmp(pAttrInfo->pszAttrName,
                      L"nTSecurityDescriptor") == 0 )
        {
            // Check the attribute type.
            if (pAttrInfo->dwADsType==ADSTYPE_NT_SECURITY_DESCRIPTOR)
            {
                pSD = (PSECURITY_DESCRIPTOR)(pAttrInfo->pADsValues->SecurityDescriptor.lpValue);
                SDSize = 
                  (pAttrInfo->pADsValues->SecurityDescriptor.dwLength);
            }
        }
        if ( _wcsicmp(pAttrInfo->pszAttrName,L"objectSID") == 0 )
        {
            // Verify the attribute type.
            if (pAttrInfo->dwADsType==ADSTYPE_OCTET_STRING)
            {
                pSID = 
                 (PSID)(pAttrInfo->pADsValues->OctetString.lpValue);
            }
        }
    }
    OBJECT_TYPE_LIST sObjectList;
    sObjectList.Level = ACCESS_OBJECT_GUID;
    sObjectList.Sbz = 0;
    
    sObjectList.ObjectType = (GUID*)&pclsid;
    
    CHAR PrivilegeSetBuffer[256];
    PRIVILEGE_SET *PrivilegeSet = (PRIVILEGE_SET *)PrivilegeSetBuffer;
    DWORD dwPrivSetSize = sizeof( PrivilegeSetBuffer );
    DWORD GrantedAccess = 0;
    ZeroMemory(PrivilegeSetBuffer, 256);
    DWORD DesiredAccess = ADS_RIGHT_DS_CONTROL_ACCESS;
    // Use the GENERIC_MAPPING structure to convert any 
    // generic access rights to object-specific access rights.
    GENERIC_MAPPING GenericMapping = DS_GENERIC_MAPPING;
    // Before calling AccessCheck, a convert must be performed
    // security descriptor into Absolute form.
    if( ! MakeAbsoluteSD(
                      pSD,
                      (PSECURITY_DESCRIPTOR)pAbsoluteSD,
                      &AbsoluteSDSize,
                      (PACL)pDacl,
                      &DaclSize,
                      (PACL)pSacl,
                      &SaclSize,
                      (PSID)pOwner,
                      &OwnerSize,
                      (PSID)pGroup,
                      &GroupSize
                      ))
    {
        pAbsoluteSD = 
           (PSECURITY_DESCRIPTOR)LocalAlloc(0,AbsoluteSDSize);
        if(!pAbsoluteSD)
        {
            // TODO: handle this.
        }
        pDacl = (PACL)LocalAlloc(0,DaclSize);
        if(!pDacl)
        {
            // TODO: handle this.
        }
        pSacl = (PACL)LocalAlloc(0,SaclSize);
        if(!pSacl)
        {
            // TODO: handle this.
        }
        pOwner = (PSID)LocalAlloc(0,OwnerSize);
        if(!pOwner)
        {
            // TODO: handle this.
        }
        pGroup = (PSID)LocalAlloc(0,GroupSize);
        if(!pGroup)
        {
            // TODO: handle this.
        }
        if( ! MakeAbsoluteSD(
                          pSD,
                          (PSECURITY_DESCRIPTOR)pAbsoluteSD,
                          &AbsoluteSDSize,
                          (PACL)pDacl,
                          &DaclSize,
                          (PACL)pSacl,
                          &SaclSize,
                          (PSID)pOwner,
                          &OwnerSize,
                          (PSID)pGroup,
                          &GroupSize
                  ))
        {
            //
            // TODO: handle this.
            //
            // Cleanup and return.
            if (pAttrInfo)
                FreeADsMem( pAttrInfo ); 
            return E_FAIL;
 
        }
    }
 
    bSuccess = AccessCheckByTypeResultList(
               pSD,            // Security descriptor
               pSID,           // SID of the verified object
               hToken,         // Handle to client access token
               DesiredAccess,  // Requested access rights 
               &sObjectList,   // An array of object types
               1,              // Number of object type elements
               &GenericMapping,// Map generic to specific rights
               PrivilegeSet,   // Receives privileges used
               &dwPrivSetSize, // Size of privilege-set buffer
               &GrantedAccess, // Retrieves mask of granted rights
               dwAccess        // Retrieves results of 
                               // access verification
               );
    // Verify that access check function call succeeded.
    if(bSuccess)
    {
        hr = S_OK;
    }
    else
        hr = E_FAIL;
}
// Use FreeADsMem for all memory obtained from ADSI call.
if (pAttrInfo)
        FreeADsMem( pAttrInfo ); 
 
return hr;
}
```



 

 




