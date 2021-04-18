---
description: Il metodo LastErrorRecord dell'oggetto Installer restituisce un oggetto record che contiene i parametri di errore per l'errore più recente della funzione che ha prodotto il record di errore.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer. LastErrorRecord, metodo
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
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324615"
---
# <a name="installerlasterrorrecord-method"></a>Installer. LastErrorRecord, metodo

Il metodo **LastErrorRecord** dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**record**](record-object.md) che contiene i parametri di errore per l'errore più recente della funzione che ha prodotto il record di errore.

## <a name="syntax"></a>Sintassi


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'oggetto [**record**](record-object.md) viene reimpostato dopo l'esecuzione di questa funzione di qualsiasi funzione che genera un record di errore.

Solo le seguenti funzioni designate generano un record di errore:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Commit**](database-commit.md)
-   [**OpenView**](database-openview.md)
-   [**Importa**](database-import.md)
-   [**Esportazione**](database-export.md)
-   [**Unione**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Execute**](view-execute.md)
-   [**Modificare**](view-modify.md)
-   [**Sestream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

Nell'esempio seguente in VBScript viene utilizzata una chiamata a [**OpenDatabase**](installer-opendatabase.md) per illustrare come ottenere informazioni estese sugli errori da uno dei metodi o delle proprietà che supportano il metodo **LastErrorRecord** . L'esempio crea un messaggio di errore quando il metodo **OpenDatabase** ha esito negativo. L'oggetto **Err** viene utilizzato per determinare se si è verificato un errore.


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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




