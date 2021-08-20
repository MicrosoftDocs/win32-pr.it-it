---
description: Il metodo LastErrorRecord dell'oggetto Installer restituisce un oggetto Record che contiene i parametri di errore per l'errore più recente dalla funzione che ha generato il record di errore.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Metodo Installer.LastErrorRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142110"
---
# <a name="installerlasterrorrecord-method"></a>Metodo Installer.LastErrorRecord

Il **metodo LastErrorRecord** dell'oggetto [**Installer**](installer-object.md) restituisce un [**oggetto Record**](record-object.md) che contiene i parametri di errore per l'errore più recente dalla funzione che ha generato il record di errore.

## <a name="syntax"></a>Sintassi


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

[**L'oggetto Record**](record-object.md) viene reimpostato dopo l'esecuzione di questa funzione di qualsiasi funzione che genera un record di errore.

Solo le funzioni designate seguenti generano un record di errore:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Eseguire il commit**](database-commit.md)
-   [**Openview**](database-openview.md)
-   [**Importa**](database-import.md)
-   [**Esportazione**](database-export.md)
-   [**Unione**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Eseguire**](view-execute.md)
-   [**Modifica**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**Targetpath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

L'esempio seguente in VBScript usa una chiamata a [**OpenDatabase**](installer-opendatabase.md) per illustrare come ottenere informazioni estese sugli errori da uno dei metodi o delle proprietà che supportano il **metodo LastErrorRecord.** L'esempio crea un messaggio di errore quando il **metodo OpenDatabase ha** esito negativo. **L'oggetto Err** viene usato per determinare se è stato rilevato un errore.


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




