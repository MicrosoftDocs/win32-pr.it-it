---
description: Nell'esempio di script seguente viene illustrata la notifica asincrona degli eventi, utilizzando il SWbemServices.Exemetodo cNotificationQueryAsync e l'oggetto SWbemSink.
ms.assetid: 8beb9804-088e-4dd1-adc8-a29ca450a220
ms.tgt_platform: multiple
title: 'Esempio: monitoraggio simultaneo di più query di eventi'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d70aff849cce81d6628b80f39e57a7f2430af056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315227"
---
# <a name="example-monitoring-multiple-event-queries-simultaneously"></a>Esempio: monitoraggio simultaneo di più query di eventi

Nell'esempio di script seguente viene illustrata la notifica asincrona degli eventi, utilizzando il [**SWbemServices.Exemetodo cNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) e l'oggetto [**SWbemSink**](swbemsink.md) .

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 


```VB
Dim WithEvents sink As SWbemSink

Private Sub ExecNoteAsync_Click()

    Dim services As SWbemServices
    Dim strQuery As String
    Dim cntxt As SWbemNamedValueSet
    Set sink = New SWbemSink
    Set services = GetObject( _
        "winmgmts:{impersonationLevel=impersonate,(security)}")
    strQuery = "SELECT * FROM __InstanceCreationEvent "& _
                "WHERE TargetInstance ISA 'Win32_NTLogEvent'"
    Set cntxt = New SWbemNamedValueSet
    cntxt.Add "sinkname", "ExecNoteAsync"
    services.Security_.Privileges.Add (wbemPrivilegeSecurity)
    services.ExecNotificationQueryAsync sink, strQuery, , , , cntxt
    MsgBox "This program will asynchronously " _
        & "process Win32_NTLogEvent events."
        
End Sub

Private Sub sink_OnObjectReady( _
             ByVal objWbemObject As WbemScripting.ISWbemObject, 
             ByVal objWbemAsyncContext As _
                 WbemScripting.ISWbemNamedValueSet)
  On Error GoTo ErrorHandler
    Dim cntxt_item As WbemScripting.SWbemNamedValue

    Set cntxt_item = objWbemAsyncContext.Item("sinkname")
        
    If cntxt_item.Value = "ExecNoteAsync" Then
        MsgBox " Got event: " & objWbemObject.TargetInstance.Message
    End If

    Set objWbemObject = Nothing

    Exit Sub                                   ' Exit to avoid handler

ErrorHandler:
    MsgBox "Error number: " & Str(Err.Number) & vbNewLine & _
    "Description: " & Err.Description, vbCritical
End Sub
```



 

 



