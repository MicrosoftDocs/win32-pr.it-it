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
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="abe8b-103">Installer. LastErrorRecord, metodo</span><span class="sxs-lookup"><span data-stu-id="abe8b-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="abe8b-104">Il metodo **LastErrorRecord** dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**record**](record-object.md) che contiene i parametri di errore per l'errore più recente della funzione che ha prodotto il record di errore.</span><span class="sxs-lookup"><span data-stu-id="abe8b-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abe8b-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="abe8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abe8b-106">Parameters</span></span>

<span data-ttu-id="abe8b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="abe8b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abe8b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abe8b-108">Return value</span></span>

<span data-ttu-id="abe8b-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="abe8b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe8b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="abe8b-110">Remarks</span></span>

<span data-ttu-id="abe8b-111">L'oggetto [**record**](record-object.md) viene reimpostato dopo l'esecuzione di questa funzione di qualsiasi funzione che genera un record di errore.</span><span class="sxs-lookup"><span data-stu-id="abe8b-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="abe8b-112">Solo le seguenti funzioni designate generano un record di errore:</span><span class="sxs-lookup"><span data-stu-id="abe8b-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="abe8b-113">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="abe8b-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="abe8b-114">**Commit**</span><span class="sxs-lookup"><span data-stu-id="abe8b-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="abe8b-115">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="abe8b-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="abe8b-116">**Importa**</span><span class="sxs-lookup"><span data-stu-id="abe8b-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="abe8b-117">**Esportazione**</span><span class="sxs-lookup"><span data-stu-id="abe8b-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="abe8b-118">**Unione**</span><span class="sxs-lookup"><span data-stu-id="abe8b-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="abe8b-119">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="abe8b-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="abe8b-120">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="abe8b-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="abe8b-121">**Execute**</span><span class="sxs-lookup"><span data-stu-id="abe8b-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="abe8b-122">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="abe8b-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="abe8b-123">**Sestream**</span><span class="sxs-lookup"><span data-stu-id="abe8b-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="abe8b-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="abe8b-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="abe8b-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="abe8b-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="abe8b-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="abe8b-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="abe8b-127">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="abe8b-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="abe8b-128">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="abe8b-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="abe8b-129">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="abe8b-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="abe8b-130">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="abe8b-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="abe8b-131">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="abe8b-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="abe8b-132">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="abe8b-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="abe8b-133">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="abe8b-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="abe8b-134">Nell'esempio seguente in VBScript viene utilizzata una chiamata a [**OpenDatabase**](installer-opendatabase.md) per illustrare come ottenere informazioni estese sugli errori da uno dei metodi o delle proprietà che supportano il metodo **LastErrorRecord** .</span><span class="sxs-lookup"><span data-stu-id="abe8b-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="abe8b-135">L'esempio crea un messaggio di errore quando il metodo **OpenDatabase** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="abe8b-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="abe8b-136">L'oggetto **Err** viene utilizzato per determinare se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="abe8b-136">The **Err** object is used to determine whether an error was encountered.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="abe8b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abe8b-137">Requirements</span></span>



| <span data-ttu-id="abe8b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe8b-138">Requirement</span></span> | <span data-ttu-id="abe8b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="abe8b-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe8b-140">Versione</span><span class="sxs-lookup"><span data-stu-id="abe8b-140">Version</span></span><br/> | <span data-ttu-id="abe8b-141">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abe8b-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="abe8b-142">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="abe8b-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="abe8b-143">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="abe8b-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="abe8b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="abe8b-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="abe8b-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe8b-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="abe8b-146">IID</span><span class="sxs-lookup"><span data-stu-id="abe8b-146">IID</span></span><br/>     | <span data-ttu-id="abe8b-147">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="abe8b-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




