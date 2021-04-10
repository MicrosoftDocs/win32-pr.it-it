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
# <a name="example-code-for-adding-a-member-to-a-group"></a><span data-ttu-id="f3c57-104">Codice di esempio per l'aggiunta di un membro a un gruppo</span><span class="sxs-lookup"><span data-stu-id="f3c57-104">Example Code for Adding a Member to a Group</span></span>

<span data-ttu-id="f3c57-105">Questo argomento contiene esempi di codice che aggiungono un membro a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-105">This topic contains code examples that add a member to a group.</span></span> <span data-ttu-id="f3c57-106">Gli esempi di Visual Basic Scripting Edition (VBScript) e C++ aggiungono un membro aggiungendo l'oggetto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) che rappresenta il membro all'oggetto [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-106">The Visual Basic Scripting Edition (VBScript) and C++ examples add a member by adding the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) object that represents the member to the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) object that represents the group.</span></span> <span data-ttu-id="f3c57-107">Negli esempi Visual Basic .NET e C# viene modificata la proprietà Member dell'oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-107">The Visual Basic .NET and C# examples modify the member property of the [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span>


<span data-ttu-id="f3c57-108">Gli esempi di codice C# seguenti aggiungono un membro esistente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-108">The following C# code examples add an existing member to a group.</span></span> <span data-ttu-id="f3c57-109">La funzione accetta l'ADsPath del contenitore del gruppo e il nome distinto del membro da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-109">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="f3c57-110">ADsPath viene utilizzato per creare un oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-110">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="f3c57-111">Il metodo [PropertyValueCollection. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) aggiunge al gruppo il membro il cui nome distinto è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="f3c57-111">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="f3c57-112">La funzione usa quindi il metodo [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) per scrivere le informazioni sul nuovo membro nel database.</span><span class="sxs-lookup"><span data-stu-id="f3c57-112">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="f3c57-113">Chiamare la funzione con i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3c57-113">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="f3c57-114">*bindString*: ADsPath valido per un contenitore del gruppo, ad esempio "LDAP://fabrikam.com/CN=TestGroup,ou=testou,DC=Fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="f3c57-114">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="f3c57-115">*nuovomembro*: nome distinto del membro da aggiungere al gruppo, ad esempio "CN = SERGIOMELCHIORI, ou = testo, DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="f3c57-115">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


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




<span data-ttu-id="f3c57-116">Gli esempi di codice di Visual Basic .NET seguenti aggiungono un membro esistente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-116">The following Visual Basic .NET code examples add an existing member to a group.</span></span> <span data-ttu-id="f3c57-117">La funzione accetta l'ADsPath del contenitore del gruppo e il nome distinto del membro da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-117">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="f3c57-118">ADsPath viene utilizzato per creare un oggetto [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-118">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="f3c57-119">Il metodo [PropertyValueCollection. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) aggiunge al gruppo il membro il cui nome distinto è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="f3c57-119">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="f3c57-120">La funzione usa quindi il metodo [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) per scrivere le informazioni sul nuovo membro nel database.</span><span class="sxs-lookup"><span data-stu-id="f3c57-120">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="f3c57-121">Chiamare la funzione con i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3c57-121">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="f3c57-122">*bindString*: ADsPath valido per un contenitore del gruppo, ad esempio "LDAP://fabrikam.com/CN=TestGroup,ou=testou,DC=Fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="f3c57-122">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="f3c57-123">*nuovomembro*: nome distinto del membro da aggiungere al gruppo, ad esempio "CN = SERGIOMELCHIORI, ou = testo, DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="f3c57-123">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


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




<span data-ttu-id="f3c57-124">Nell'esempio VBScript seguente viene aggiunto un membro esistente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-124">The following VBScript example adds an existing member to a group.</span></span> <span data-ttu-id="f3c57-125">Lo script aggiunge l'utente Jeff Smith al gruppo TestGroup.</span><span class="sxs-lookup"><span data-stu-id="f3c57-125">The script adds the user, Jeff Smith, to the TestGroup group.</span></span>


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




<span data-ttu-id="f3c57-126">Nell'esempio di codice C++ riportato di seguito viene aggiunto un membro esistente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3c57-126">The following C++ code example adds an existing member to a group.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f3c57-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3c57-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c57-128">Aggiunta di membri a gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="f3c57-128">Adding Members to Groups in a Domain</span></span>](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[<span data-ttu-id="f3c57-129">DirectoryEntry</span><span class="sxs-lookup"><span data-stu-id="f3c57-129">DirectoryEntry</span></span>](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[<span data-ttu-id="f3c57-130">DirectoryEntry. CommitChanges</span><span class="sxs-lookup"><span data-stu-id="f3c57-130">DirectoryEntry.CommitChanges</span></span>](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[<span data-ttu-id="f3c57-131">**IADs**</span><span class="sxs-lookup"><span data-stu-id="f3c57-131">**IADs**</span></span>](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="f3c57-132">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="f3c57-132">**IADsGroup**</span></span>](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="f3c57-133">PropertyValuecollection. Add</span><span class="sxs-lookup"><span data-stu-id="f3c57-133">PropertyValueCollection.Add</span></span>](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 