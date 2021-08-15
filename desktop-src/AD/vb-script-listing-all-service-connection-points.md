---
title: VB Script che elenca tutti i punti di connessione del servizio
ms.assetid: 7a76f872-3e4e-4bb7-8f2d-e30b1246369f
ms.tgt_platform: multiple
description: 'Altre informazioni su: Script VB elencare tutti i punti di connessione del servizio'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6872a8a516d7f6a75cd25ddb6970b0830775fb881f0a0f601756021e2264072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182265"
---
# <a name="vb-script-listing-all-service-connection-points"></a>VB Script che elenca tutti i punti di connessione del servizio

I punti di connessione del servizio possono essere gestiti VB script. Il codice di esempio seguente illustra come elencare tutti i punti di connessione del servizio nel nome di dominio specificato nella riga di comando:


```VB
Option Explicit

Dim scpDN
scpDN = WScript.Arguments.Named("SCP")

If ( scpDN = "" ) Then
    Usage
Else
    ScpProperties scpDN
End If

' End of Main

Sub Usage
    WScript.Echo "USAGE:  ScpProperties /SCP:<SCP DN>"
    WScript.Echo ""
    Wscript.Echo "Remember to put the SCP DN between quotes"
End Sub

Sub ScpProperties( strDN )

    Dim oConn ' As ADODB.Connection
    Set oConn = CreateObject("ADODB.Connection")
    
    oConn.Open "Provider=ADsDSOObject"
    
    Dim oCmd ' As ADODB.Command
    Set oCmd = CreateObject("ADODB.Command")
    oCmd.ActiveConnection = oConn
    
    ' In the next command, the real magic is in knowing LDAP queries
    ' GC means to ask the global catalog.
    oCmd.CommandText = "<GC://" & strDN & ">;" & _
                        "(objectClass=ServiceConnectionPoint);" & _
                        "distinguishedname,name,serviceDNSName," & _
                        "serviceDNSNameType,serviceBindingInformation," & _
                        "serviceClassName,Keywords;" & _
                        "subtree"

    Dim oRs ' As ADODB.Recordset
    Set oRs = oCmd.Execute
    
    Dim lCount ' As Long
    lCount = 0
    Do While (Not oRs.EOF)
    
        Wscript.Echo "SCP Name: " & oRs("name")
        Wscript.Echo "DN: " & oRs("distinguishedname")
        Wscript.Echo "serviceDNSName: " & oRs("serviceDNSName")
        Wscript.Echo "serviceDNSNameType: " & oRs("serviceDNSNameType")
        Wscript.Echo "serviceClassName: " & oRs("serviceClassName")
        Dim a ' As Variant
        Dim l 'As Long
        
        a = oRs("serviceBindingInformation")
        
        If (Not IsNull(a)) Then
            Wscript.Echo "serviceBindingInformation:"
            For l = LBound(a) To UBound(a)
                Wscript.Echo vbTab & a(l)
            Next
            Wscript.Echo 
        End If
        
        a = oRs("Keywords")
        If (Not IsNull(a)) Then
            Wscript.Echo "Keywords: "
            For l = LBound(a) To UBound(a)
                Wscript.Echo vbTab & a(l)
            Next
        End If
        
        oRs.MoveNext
        lCount = lCount + 1
        Wscript.Echo 
    Loop
    
    Wscript.Echo "Total objects = " & lCount
    oConn.Close
    
End Sub
    
```



 

 




