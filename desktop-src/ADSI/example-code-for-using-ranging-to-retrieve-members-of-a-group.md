---
title: Codice di esempio per l'uso di Ranging per recuperare i membri di un gruppo
description: Nell'esempio di codice seguente viene utilizzato con ActiveX Directory Objects (ADO) per recuperare i membri di un gruppo.
ms.assetid: baebefd5-7ac6-4d36-a5a4-0796d790abee
ms.tgt_platform: multiple
keywords:
- Codice di esempio per l'utilizzo di Ranging per recuperare i membri di un gruppo ADSI
- codice di esempio C/C++ ADSI, usando ranging per recuperare i membri di un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d68920d19135387ec76003ca621472ea9266102d84930e4af84e13b886335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691844"
---
# <a name="example-code-for-using-ranging-to-retrieve-members-of-a-group"></a>Codice di esempio per l'uso di Ranging per recuperare i membri di un gruppo

Nell'esempio di codice seguente viene utilizzato con ActiveX Directory Objects (ADO) per recuperare i membri di un gruppo.

Il frammento di codice seguente richiede un riferimento a Microsoft ActiveX Data Objects 6.0 Library.


```VB
 Private Sub EnumGroupWithADO(ByVal strGroupDN As String, ByVal strUsername As String, ByVal strPassword As String)
        Dim oConn
        Dim oComm
        Dim rangeStep
        Dim lowRange
        Dim highRange
        Dim lastLoop
        Dim commandPrefix
        Dim amp
        Dim commandSuffix
        Dim oRS
        Dim nRetrieved
        oConn = CreateObject("ADODB.Connection")
        oComm = CreateObject("ADODB.Command")

        oConn.Provider = "ADsDSOObject"
        oConn.Properties("ADSI Flag") = 1

        If strUsername <> "" Then
            oConn.Properties("User ID") = strUsername
            oConn.Properties("Password") = strPassword
        End If

        oConn.Open()
        oComm.ActiveConnection = oConn

        ' For compatibility with all operating systems, the number of objects
        ' retrieved by each query should not exceed 999.
        rangeStep = 999

        lastLoop = False
        lowRange = 0
        highRange = lowRange + rangeStep

        commandPrefix = "<LDAP://" & strGroupDN > ">;(objectClass=*);member;range="
        commandSuffix = ";base"

        Do
            If lastLoop Then
                ' Perform this query with the "range=<lowRange>-*" range.
                oComm.CommandText = commandPrefix & lowRange & "-*" & commandSuffix
            Else
                ' Perform this query with the "range=<lowRange>-<highRange>" range.
                oComm.CommandText = commandPrefix & lowRange & "-" & highRange & commandSuffix
            End If
            Debug.Print("Current search command: " & oComm.CommandText)

            ' Execute the query.
            oRS = oComm.Execute

            ' Reset the retrieved members counter.
            nRetrieved = 0

            ' Enumerate the retrieved members.
            While Not oRS.EOF
                For Each oField In oRS.Fields
                    If VarType(oField) = (vbArray + vbVariant) Then
                        For Each oValue In oField.Value
                            Debug.Print(vbTab & oValue)
                            nRetrieved = nRetrieved + 1
                        Next
                    End If
                Next
                oRS.MoveNext()
            End While

            ' If the last query was performed, exit the loop.
            If lastLoop = True Then
                Exit Do
            End If

            If nRetrieved = 0 Then
                ' No objects were retrieved by the last query; perform one last query
                ' with the â€œrange=<lowRange>-*â€ range.
                lastLoop = True
            Else
                ' Increment the high and low ranges to query for the next block of objects.
                lowRange = highRange + 1
                highRange = lowRange + rangeStep
            End If
        Loop While nRetrieved = lowRange
    End Sub
End Module
```



 

 




