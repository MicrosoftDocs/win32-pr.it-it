---
title: Codice di esempio per la ricerca di gruppi in un dominio
description: Questo argomento include un esempio di codice che cerca nel sottoalbero del contenitore specificato tutti gli oggetti gruppo con il tipo di gruppo specificato.
ms.assetid: 07b27324-4f59-42c2-a42f-8c2cef138928
ms.tgt_platform: multiple
keywords:
- Active Directory esempi di Active Directory, ricerca di gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15d2e0957032202e2080f85c71631daeddec70817ec09eb8432415aba47b3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693340"
---
# <a name="example-code-for-searching-for-groups-in-a-domain"></a>Codice di esempio per la ricerca di gruppi in un dominio

L'esempio di codice C/C++ seguente cerca nel sottoalbero del contenitore specificato tutti gli oggetti gruppo con il tipo di gruppo specificato.


```C++
/***************************************************************************

    PrintGroupsInContainer()

    Searches the entire subtree for all groups objects that contain the 
    specified group type bits from the ADS_GROUP_TYPE_ENUM enumeration.

***************************************************************************/

HRESULT PrintGroupsInContainer(LPCWSTR pwszContainerDN, DWORD type)
{
    HRESULT hr = E_FAIL;

    // Construct the ADsPath to bind to the search root.
    CComBSTR sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszContainerDN;

    // Bind to the container.
    CComPtr<IDirectorySearch> spSearch;
    hr = ADsGetObject(sbstrADsPath, IID_IDirectorySearch, (LPVOID*)&spSearch);
    if(SUCCEEDED(hr))
    {
        ADS_SEARCHPREF_INFO SearchPref[1];

        // Set the scope of the search to be all of the subtree.
        SearchPref[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
        SearchPref[0].vValue.dwType = ADSTYPE_INTEGER;
        SearchPref[0].vValue.Integer = ADS_SCOPE_SUBTREE;

        hr = spSearch->SetSearchPreference(SearchPref, sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO));
        if(FAILED(hr))
        {
            return hr;
        }

        ADS_SEARCH_HANDLE hSearch = NULL;
        LPWSTR pwszDN = L"distinguishedName";
        LPWSTR pwszAttributes[1] = {pwszDN};
        
        // Convert the group type to search for into a string.
        WCHAR wszGroupType[30]; // Plenty large enough to handle the biggest 32-bit number.
        swprintf_s(wszGroupType, L"%d", type);

        // Construct the search filter.
        CComBSTR sbstrSearchFilter;
        sbstrSearchFilter = "(&(objectClass=group)(groupType:";
        sbstrSearchFilter += LDAP_MATCHING_RULE_BIT_AND;
        sbstrSearchFilter += ":=";
        sbstrSearchFilter += wszGroupType;
        sbstrSearchFilter += "))";

        // Execute the search.
        hr = spSearch->ExecuteSearch(sbstrSearchFilter, 
            pwszAttributes, 
            sizeof(pwszAttributes)/sizeof(LPWSTR), 
            &hSearch);

        if(FAILED(hr))
        {
            return hr;
        }
        
        // Get the first result row. There should never be more than one result.
        hr = spSearch->GetFirstRow(hSearch);
        while(S_OK == hr)
        {
            ADS_SEARCH_COLUMN col;
            
            // Get the distinguished name for the current result.
            hr = spSearch->GetColumn(hSearch, pwszDN, &col);
            if(SUCCEEDED(hr))
            {
                if(ADSTYPE_DN_STRING  == col.dwADsType)
                {
                    wprintf(col.pADsValues[0].DNString);
                    wprintf(L"\n\n");
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
            
            hr = spSearch->GetNextRow(hSearch);
        }

        // Close the search handle to cleanup.
        hr = spSearch->CloseSearchHandle(hSearch);
    }
    
    return hr;
}
```



Nell'esempio Visual Basic codice seguente viene eseguita una ricerca nel sottoalbero del contenitore specificato per tutti gli oggetti gruppo con il tipo di gruppo specificato.


```VB
''''''''''''''''''''''''''''''''''''''''
'   PrintGroupsInContainer()
'
'   Searches the entire subtree for all groups objects that contain the
'   specified group type bits from the ADS_GROUP_TYPE_ENUM enumeration.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub PrintGroupsInContainer(ContainerDN As String, GroupType As Long)
    Const ADS_GROUP_TYPE_GLOBAL_GROUP = 2
    Const ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP = 4
    Const ADS_GROUP_TYPE_LOCAL_GROUP = 4
    Const ADS_GROUP_TYPE_UNIVERSAL_GROUP = 8
    Const ADS_GROUP_TYPE_SECURITY_ENABLED = &H80000000
    
    Const ADS_SECURE_AUTHENTICATION = 1
    
    Const LDAP_MATCHING_RULE_BIT_AND = "1.2.840.113556.1.4.803"
    Const LDAP_MATCHING_RULE_BIT_OR = "1.2.840.113556.1.4.804"
    
    Set oConn = CreateObject("ADODB.Connection")
    Set oComm = CreateObject("ADODB.Command")
     
    oConn.Provider = "ADsDSOObject"
    oConn.Properties("ADSI Flag") = ADS_SECURE_AUTHENTICATION
    
    oConn.Open
    oComm.ActiveConnection = oConn
    
    oComm.CommandText = "<LDAP://" + ContainerDN + ">;(&(objectClass=group)(groupType:" + LDAP_MATCHING_RULE_BIT_AND + ":=" + str(GroupType) + "));distinguishedName;subtree"
    
    ' Execute the query.
    Set oRS = oComm.Execute
    
    ' Print the results.
    oRS.MoveFirst
    While Not oRS.EOF
        List.AddItem oRS.Fields(0)
        
        oRS.MoveNext
    Wend
End Sub
```



 

 




