---
description: Il metodo FormatRecord dell'oggetto Session restituisce una stringa formattata da un modello e registra i dati.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. FormatRecord, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327791"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="8c0d3-103">Session. FormatRecord, metodo</span><span class="sxs-lookup"><span data-stu-id="8c0d3-103">Session.FormatRecord method</span></span>

<span data-ttu-id="8c0d3-104">Il metodo **FormatRecord** dell'oggetto [**Session**](session-object.md) restituisce una stringa formattata da un modello e registra i dati.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c0d3-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="8c0d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c0d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0d3-107">*record*</span><span class="sxs-lookup"><span data-stu-id="8c0d3-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0d3-108">Oggetto **record** obbligatorio contenente un modello e i dati da formattare.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="8c0d3-109">La stringa di modello deve essere impostata nel campo 0 seguito da qualsiasi parametro di dati a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0d3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c0d3-110">Return value</span></span>

<span data-ttu-id="8c0d3-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0d3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c0d3-112">Remarks</span></span>

<span data-ttu-id="8c0d3-113">Il metodo **FormatRecord** usa il processo di formato seguente.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="8c0d3-114">I parametri da [formattare](formatted.md) sono racchiusi tra parentesi quadre \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="8c0d3-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="8c0d3-115">È possibile scorrere le parentesi quadre perché le sostituzioni vengono risolte dall'interno.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="8c0d3-116">Se una parte della stringa è racchiusa tra parentesi graffe {} e non contiene parentesi quadre, la parte viene lasciata invariata, comprese le parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="8c0d3-117">Se una parte della stringa è racchiusa tra parentesi graffe e contiene uno o più nomi di proprietà e se vengono trovate tutte le proprietà, il testo (con le sostituzioni risolte) viene visualizzato senza le parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="8c0d3-118">Se una qualsiasi delle proprietà non viene trovata, tutto il testo racchiuso tra parentesi graffe e parentesi graffe vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="8c0d3-119">**Per formattare le stringhe usando il metodo FormatRecord**</span><span class="sxs-lookup"><span data-stu-id="8c0d3-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="8c0d3-120">I parametri numerici vengono sostituiti sostituendo il marcatore con il valore del campo record corrispondente, con valori mancanti o null che non producono testo.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="8c0d3-121">La stringa risultante viene elaborata sostituendo i parametri non record con i valori corrispondenti, come indicato nelle descrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="8c0d3-122">Se viene rilevata una sottostringa nel formato " \[ PropertyName \] ", questa viene sostituita dal valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="8c0d3-123">Se viene trovata una sottostringa nel formato " \[ % Metodo EnvironmentVariable \] ", il valore della variabile di ambiente viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="8c0d3-124">Se viene trovata una sottostringa del modulo \[ \# *FileKey* \] , questa viene sostituita dal percorso completo del file, con il valore *FileKey* usato come chiave nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="8c0d3-125">Il valore di \[ \# *FileKey* \] rimane vuoto e non viene sostituito da un percorso fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="8c0d3-126">Il valore di \[ \# *FileKey* \] dipende dallo stato di installazione del componente a cui appartiene il file.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="8c0d3-127">Se il componente viene eseguito dall'origine, il valore è il percorso della posizione di origine del file.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="8c0d3-128">Se il componente viene eseguito localmente, il valore è il percorso della posizione di destinazione del file dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="8c0d3-129">Se il componente è assente, il percorso è vuoto.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="8c0d3-130">Per ulteriori informazioni sul controllo dello stato di installazione dei componenti di, vedere [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="8c0d3-131">Se viene trovata una sottostringa del modulo \[ *$componentkey* \] , questa viene sostituita dalla directory di installazione del componente, con il valore *componentkey* usato come chiave nella tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="8c0d3-132">Il valore di \[ $ *componentkey* \] rimane vuoto e non viene sostituito da una directory fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="8c0d3-133">Il valore di \[ $ *componentkey* \] dipende dallo stato di installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="8c0d3-134">Se il componente viene eseguito dall'origine, il valore è la directory di origine del file.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="8c0d3-135">Se il componente viene eseguito localmente, il valore è la directory di destinazione dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="8c0d3-136">Se il componente è assente, il valore viene lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="8c0d3-137">Per ulteriori informazioni sul controllo dello stato di installazione dei componenti di, vedere [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="8c0d3-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="8c0d3-138">Se viene trovata una sottostringa nel formato " \[ \\ c \] ", questa viene sostituita dal carattere senza ulteriori elaborazioni.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="8c0d3-139">Viene mantenuto solo il primo carattere dopo la barra rovesciata; tutte le altre operazioni vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0d3-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c0d3-140">Requirements</span></span>



| <span data-ttu-id="8c0d3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c0d3-141">Requirement</span></span> | <span data-ttu-id="8c0d3-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8c0d3-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0d3-143">Versione</span><span class="sxs-lookup"><span data-stu-id="8c0d3-143">Version</span></span><br/> | <span data-ttu-id="8c0d3-144">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8c0d3-145">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c0d3-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8c0d3-146">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c0d3-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8c0d3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8c0d3-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c0d3-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c0d3-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8c0d3-149">IID</span><span class="sxs-lookup"><span data-stu-id="8c0d3-149">IID</span></span><br/>     | <span data-ttu-id="8c0d3-150">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8c0d3-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="8c0d3-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c0d3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0d3-152">Formattato</span><span class="sxs-lookup"><span data-stu-id="8c0d3-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="8c0d3-153">Tipi di dati delle colonne</span><span class="sxs-lookup"><span data-stu-id="8c0d3-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




