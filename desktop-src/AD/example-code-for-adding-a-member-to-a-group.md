---
title: Codice di esempio per l'aggiunta di un membro a un gruppo
description: Questo argomento contiene esempi di codice che aggiungono un membro a un gruppo.
ms.assetid: 306fcadb-a492-41e5-bfb3-8beaaec24fb5
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, aggiunta di un membro a un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a64a41fac871c6793ee4d0db1f4be79c9fbd0d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963564"
---
# <a name="example-code-for-adding-a-member-to-a-group"></a>Codice di esempio per l'aggiunta di un membro a un gruppo

Questo argomento contiene esempi di codice che aggiungono un membro a un gruppo. Gli esempi di Visual Basic Scripting Edition (VBScript) e C++ aggiungono un membro aggiungendo l'oggetto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) che rappresenta il membro all'oggetto [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) che rappresenta il gruppo. Negli esempi Visual Basic .NET e C# viene modificata la proprietà Member dell'oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo.


Gli esempi di codice C# seguenti aggiungono un membro esistente a un gruppo. La funzione accetta l'ADsPath del contenitore del gruppo e il nome distinto del membro da aggiungere al gruppo. ADsPath viene utilizzato per creare un oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo. Il metodo [PropertyValueCollection. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) aggiunge al gruppo il membro il cui nome distinto è stato passato alla funzione. La funzione usa quindi il metodo [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) per scrivere le informazioni sul nuovo membro nel database.

Chiamare la funzione con i parametri seguenti:

-   *bindString*: ADsPath valido per un contenitore del gruppo, ad esempio "LDAP://fabrikam.com/CN=TestGroup,ou=testou,DC=Fabrikam,DC=com"
-   *nuovomembro*: nome distinto del membro da aggiungere al gruppo, ad esempio "CN = SERGIOMELCHIORI, ou = testo, DC = Fabrikam, DC = com"


```CSharp
private void AddMemberToGroup(

                                string bindString,

                                string newMember

                                )

{

    try
    {

        DirectoryEntry ent = new DirectoryEntry( bindString );

        ent.Properties["member"].Add(newMember);

        ent.CommitChanges();

    }

    catch (Exception e)
    {

        Console.WriteLine( "An error occurred.");

        Console.WriteLine( "{0}", e.Message);

        return;

    }

}
```




Gli esempi di codice di Visual Basic .NET seguenti aggiungono un membro esistente a un gruppo. La funzione accetta l'ADsPath del contenitore del gruppo e il nome distinto del membro da aggiungere al gruppo. ADsPath viene utilizzato per creare un oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo. Il metodo [PropertyValueCollection. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) aggiunge al gruppo il membro il cui nome distinto è stato passato alla funzione. La funzione usa quindi il metodo [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) per scrivere le informazioni sul nuovo membro nel database.

Chiamare la funzione con i parametri seguenti:

-   *bindString*: ADsPath valido per un contenitore del gruppo, ad esempio "LDAP://fabrikam.com/CN=TestGroup,ou=testou,DC=Fabrikam,DC=com"
-   *nuovomembro*: nome distinto del membro da aggiungere al gruppo, ad esempio "CN = SERGIOMELCHIORI, ou = testo, DC = Fabrikam, DC = com"


```VB
Private Sub AddMemberToGroup(ByVal bindString As String, 
                                      ByVal newMember As String)

    Try

        Dim ent As New DirectoryEntry(bindString)

        ent.Properties("member").Add(newMember)

        ent.CommitChanges()

    Catch e As Exception

        Console.WriteLine("An error occurred.")

        Console.WriteLine("{0}", e.Message)

        Return

    End Try

End Sub
```




Nell'esempio VBScript seguente viene aggiunto un membro esistente a un gruppo. Lo script aggiunge l'utente Jeff Smith al gruppo TestGroup.


```VB
Option Explicit

On Error Resume Next

Dim scriptResult        ' Script success or failure

Dim groupPath           ' ADsPath to the group container

Dim group               ' Group object

Dim memberPath          ' ADsPath to the member

Dim member              ' Member object

Dim groupMemberList     ' Used to display group members

Dim errorText           ' Error handing text

scriptResult = False

groupPath = "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"

memberPath = "LDAP://CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"

WScript.Echo("Retrieving group object")

Set group = GetObject(groupPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not create group object.")

End If

Call ShowMembers(groupPath)     'Optional function call

WScript.Echo("Retrieving new member object")

Set member = GetObject(memberPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not get new member object.")

End If

WScript.Echo("Adding member to group.")

group.Add(member.ADsPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not add member to group.")

End If

Call ShowMembers(groupPath)     ' Optional function call

scriptResult = True

Call FinalResult(scriptResult)

'****************************************************************
' This function displays the members of a group. The function
' takes the ADsPath of the group.
'****************************************************************

Sub ShowMembers(groupPath)

    Dim groupMember

    Dim groupMemberList

    Dim groupObject

    Set groupObject = GetObject(groupPath)

    Set groupMemberList = groupObject.Members

    Select Case groupMemberList.Count

        Case 1 

            WScript.Echo vbcrlf & "The group has one member."

        Case 0

            WScript.Echo vbcrlf & "The group has no members."

        Case Else

            WScript.Echo vbcrlf & "The group has " & groupMemberList.Count & " members."

    End Select

    If groupMemberList.Count > 0 then

        WScript.Echo vbcrlf & "Here is a member list."

        For Each groupMember in groupMemberList

            WScript.Echo groupMember.Name

        Next

        WScript.Echo vbcrlf

    End If

    Set groupObject = Nothing

    Set groupMemberList = Nothing

End Sub

'****************************************************************
' This function shows if the script succeeded or failed. The 
' function processed the scriptResult variable.
'****************************************************************

Sub FinalResult(scriptResult)

    WScript.Echo vbcrlf

    If scriptResult = False then

        WScript.Echo "Script failed."

    Else

        WScript.Echo("Script successfully completed.")

    End If

    WScript.Quit

End Sub

'****************************************************************
' This function handles errors that occur in the script.
'****************************************************************

Sub ErrorHandler( errorText )

    WScript.Echo(vbcrlf & errorText)

    WScript.Echo("Error number: " & Err.number)

    WScript.Echo("Error Description: " & Err.Description)

    Err.Clear 

    Call FinalResult(scriptResult)

End Sub

```




Nell'esempio di codice C++ riportato di seguito viene aggiunto un membro esistente a un gruppo.


```C++
/////////////////////////////////////////////////////////////
/*  AddMemberToGroup() - Adds the passed directory object as a member 
                         of passed group
 
    Parameters
 
        IADsGroup * pGroup   - Group to hold the new IDirectoryObject.
        IADs* pIADsNewMember - Object which will become a member 
                               of the group. Object can be a user, 
                               contact, or group.
*/
HRESULT AddMemberToGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath.
    // When the ADsPath string is returned, to add the new
    // member to the group, call the IADsGroup::Add() member,
    // passing in the ADsPath string.
    // Query the new member for its AdsPath.
    // This is a fully qualified LDAP path to the object to add.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to add the new member.
        // Pass the LDAP path to the 
        // new member to the IADsGroup::Add() member
        hr = pGroup->Add(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di membri a gruppi in un dominio](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[**IADs**](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[PropertyValuecollection. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 