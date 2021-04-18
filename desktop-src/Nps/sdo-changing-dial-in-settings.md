---
title: Modifica delle impostazioni di connessione remota
description: Modifica delle impostazioni di connessione remota
ms.assetid: db9d6d1c-2317-40ed-832b-f72f8e9e81bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d2759ce57651b393debb810f534310c24f7a74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299869"
---
# <a name="changing-dial-in-settings"></a><span data-ttu-id="5d1fd-103">Modifica delle impostazioni di connessione remota</span><span class="sxs-lookup"><span data-stu-id="5d1fd-103">Changing Dial-In Settings</span></span>

<span data-ttu-id="5d1fd-104">Il codice VBScript seguente imposta il bit di connessione e il numero di callback per un utente.</span><span class="sxs-lookup"><span data-stu-id="5d1fd-104">The following VBScript code sets the dial-in bit and callback number for a user.</span></span>


```VB
Set shell = wscript.createobject ("WScript.Shell")
Set environment = shell.environment ("PROCESS")

userdomain    = environment.Item ("USERDOMAIN")
logonserver   = environment.Item ("LOGONSERVER")
userdnsdomain = environment.Item ("USERDNSDOMAIN")
computername  = environment.Item ("COMPUTERNAME")

commands=wscript.arguments.count

Dim user
Dim machine

server = ""
number = ""
name   = ""
dialin = ""

For Each command In wscript.arguments
    lccommand=lcase(command)
    If instr(lccommand,"/server:") Then server = Mid(command,9)
    If instr(lccommand,"/user:")   Then name   = Mid(command,7)
    If instr(lccommand,"/dialin:") Then dialin = Mid(command,9)
    If instr(lccommand,"/number:") Then number = Mid(command,9)
    If instr(lccommand,"?") or instr(lccommand,"/help") Then
        showhelp=True
    End If
Next

If (server = "") Then server = computername
If (name = "") Then showhelp = True
If (dialin = "") AND (number = "") Then showhelp = True
If (number = "NONE") Then number = ""

If showhelp Then
    wscript.echo "SETDIALINCALLBACK"
    wscript.echo "Set the Dialin value (Allow, Deny or RAS Policy) and callback number for a user"
    wscript.echo "Setdialincallback /user:<username> /server:<server> /dialin:<ALLOW|DENY|RAS> /number:<NONE|""number"">"
    wscript.echo ""
Else
    Initialize server, name
    If err <>0 Then 
        Wscript.Echo "Failed to Initialize." 
            If hex(err) = "800708AD" Then
                wscript.echo "(" & hex(err) & ") " & "The user name could not be found."
            Else
                wscript.echo "(" & hex(err) & ") " & err.description
                wscript.quit(err)
            End If
    End If

    If (dialin <> "") Then 
        SetDialin dialin
        If err <>0 Then 
            Wscript.Echo "Failed to Set the dialin." 
            wscript.echo "(" & hex(err) & ") " & err.description
            wscript.quit(err)
        End If
    End If

    SetCallback number
    If err <>0 Then 
        Wscript.Echo "Failed to Set the callback." 
        wscript.echo "(" & hex(err) & ") " & err.description
        wscript.quit(err)
    End If

    RasInfo server, name
    If err <> 0 Then 
        Wscript.Echo "Failed to get the user options." 
        If hex(err) = "800708AD" Then
            wscript.echo "(" & hex(err) & ") " & "The user name could not be found."
        Else
            wscript.echo "(" & hex(err) & ") " & err.description
        End If
        wscript.quit(err)
    End If
End If

'
' Subroutine Definitions
'
Sub Initialize(server, name)

    Set machine = createobject("IAS.SDOMachine")
    machine.attach(server)
    Set user = machine.getusersdo(0,name) '0 for DATA_STORE_LOCAL

End Sub


Sub SetDialin(dialin)

    Select Case dialin
        case "ALLOW"                    ' "Allow access."
            user.putproperty 1032,true  

        case "DENY"                     ' "Deny access."
            user.putproperty 1032,false  

        case "RAS"                      ' "Control access through Remote Access Policy."
            user.putproperty 1032, Empty 
    End Select

    user.Apply

End Sub


Sub SetCallback(number)
    
    Dim lValue

    If (number <> "") Then
        user.putproperty 1026,number    ' msRADIUSCallbackNumber
        user.putproperty 1029,number    ' msRASSavedCallbackNumber 
                                        ' 1033 callback policy NP_CONSTRAINT or PROPERTY_USER_SERVICE_TYPE
        lValue = CLng(4)                ' 4 = always callback
        user.putproperty 1033, lValue
    Else
        user.putproperty 1026,lValue    ' msRADIUSCallbackNumber
        user.putproperty 1029,lValue    ' msRASSavedCallbackNumber 
        user.putproperty 1033,lValue    ' no callback
    End If

    user.Apply

End Sub


Sub RasInfo(server,name)

    Dim novalue
    
    Set t = createobject("IAS.SDOMachine")
    t.attach(server)

    cid = Array(cidnumber)

    If cidnumber="NONE" Then cid=novalue

    Set mach1 = GetObject("WinNT://" & server & ",Computer")

    Set g1 = mach1.GetObject("Group","Users")
    Set g = g1.Members()

    Set u = t.getusersdo(0,Name)

    msg = "Name: " & u.getproperty(2) & vbcrlf
    msg = msg & "--------------------------------------" & vbcrlf


    '1032
    dperm=u.getproperty(1032)
    If dperm = True  Then dialin = "Allow access."
    If dperm = False Then dialin = "Deny access."
    If isempty (dperm) Then dialin = "Control access through Remote Access Policy."
    msg = msg & dialin & vbcrlf

    a=1024                                  'callerid. 1025 is saved value
    v=u.getproperty(a)
    
    If isarray(v) Then
        For Each e In v
            msg = msg & "VerIfy Caller-ID: " & e & vbcrlf
        next
    Else
        msg = msg & "VerIfy Caller-ID: " & vbcrlf
    End If

    a=1026                                  'callback. 1033 callback policy
    cbmode = "No Callback"
    If u.getproperty(1033) > 0 Then
        cbstring = u.getproperty(1026) & ""
        cbmode = "Always call back to: " & cbstring
        If  cbstring = "" Then cbmode = "Set by caller."
    End If
    msg = msg & cbmode
    
    wscript.echo msg

    Set mach = GetObject("WinNT://" & server & ",Computer")
    If IsEmpty (mach) Then
        wscript.echo "Can't get to computer " & machName & "." 
        Exit Sub
    End If

    err.clear
    Set usr = mach.GetObject ("user",name)
    flags = Clng(usr.Get("UserFlags"))

    ADS_UF_SCRIPT                           =  &H0001&
    ADS_UF_ACCOUNTDISABLE                   =  &H0002&
    ADS_UF_HOMEDIR_REQUIRED                 =  &H0003&
    ADS_UF_LOCKOUT                          =  &H0010&
    ADS_UF_PASSWD_NOTREQD                   =  &H0020&
    ADS_UF_PASSWD_CANT_CHANGE               =  &H0040&
    ADS_UF_TEMP_DUPLICATE_ACCOUNT           =  &H0100&
    ADS_UF_NORMAL_ACCOUNT                   =  &H0200&
    ADS_UF_INTERDOMAIN_TRUST_ACCOUNT        =  &H0800&
    ADS_UF_WORKSTATION_TRUST_ACCOUNT        =  &H1000&
    ADS_UF_SERVER_TRUST_ACCOUNT             =  &H2000&
    ADS_UF_DONTEXPIREPASSWD                 =  &H10000&
    ADS_UF_MNS_LOGON_ACCOUNT                =  &H20000&
    ADS_UF_SMARTCARD_REQUIRED               =  &H40000&
    ADS_UF_TRUSTED_FOR_DELEGATION           =  &H80000&
    ADS_UF_NOT_DELEGATED                    =  &H100000&

    expired = usr.Get ("PasswordExpired")
    
    wscript.echo "User must change password: " & CBOOL(expired)
    wscript.echo "User cannot change password: " & CBOOL(flags AND ADS_UF_PASSWD_CANT_CHANGE)
    wscript.echo "Password never expires: " & CBOOL(flags AND ADS_UF_DONT_EXPIRE_PASSWD)
    wscript.echo "Account disabled: " & CBOOL(flags AND ADS_UF_ACCOUNTDISABLE)
    wscript.echo "Account locked out: " & CBOOL(flags AND ADS_UF_LOCKOUT)
    wscript.echo "Password not required: " & CBOOL(flags AND ADS_UF_PASSWD_NOTREQD)

End Sub
```



## <a name="related-topics"></a><span data-ttu-id="5d1fd-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d1fd-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d1fd-106">**CLIENTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="5d1fd-106">**CLIENTPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-clientproperties)
</dt> <dt>

[<span data-ttu-id="5d1fd-107">Enumerazione di oggetti in una raccolta</span><span class="sxs-lookup"><span data-stu-id="5d1fd-107">Enumerating Objects in a Collection</span></span>](/windows/desktop/Nps/sdo-enumerating-objects-in-a-collection)
</dt> <dt>

[<span data-ttu-id="5d1fd-108">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="5d1fd-108">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="5d1fd-109">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="5d1fd-109">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="5d1fd-110">**ISdoMachine**</span><span class="sxs-lookup"><span data-stu-id="5d1fd-110">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="5d1fd-111">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="5d1fd-111">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)
</dt> </dl>

 

 