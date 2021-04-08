---
description: 'WsdCodeGen ha due funzioni: la generazione di file di configurazione e la generazione di codice sorgente per applicazioni host e client WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Sintassi della riga di comando di WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880394"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="8642d-103">Sintassi della riga di comando di WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="8642d-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="8642d-104">WsdCodeGen ha due funzioni: la generazione di file di configurazione e la generazione di codice sorgente per applicazioni host e client WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8642d-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="8642d-105">In questo argomento viene illustrata la sintassi della riga di comando utilizzata per eseguire ogni attività.</span><span class="sxs-lookup"><span data-stu-id="8642d-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="8642d-106">Generazione di un file di configurazione</span><span class="sxs-lookup"><span data-stu-id="8642d-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="8642d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8642d-107">Syntax</span></span>

<span data-ttu-id="8642d-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client** \| **host** \| **All**} **\[ /outputfile:**_nomefileconfigurazione_ *_\]_* *WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="8642d-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="8642d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8642d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8642d-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: { \| host client \| All}**</span><span class="sxs-lookup"><span data-stu-id="8642d-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="8642d-111">Tipo di codice che il file di configurazione di output genererà.</span><span class="sxs-lookup"><span data-stu-id="8642d-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="8642d-112">**/generateconfig: il client** viene usato per generare un file di configurazione per la generazione di codice client, **/generateconfig: host** viene usato per generare un file di configurazione per la generazione del codice host e **/generateconfig: All** viene usato per generare un file di configurazione per la generazione di codice client e host.</span><span class="sxs-lookup"><span data-stu-id="8642d-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_nomefileconfigurazione_</span><span class="sxs-lookup"><span data-stu-id="8642d-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="8642d-114">Questo parametro facoltativo viene utilizzato per specificare il nome file del file di configurazione di output.</span><span class="sxs-lookup"><span data-stu-id="8642d-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="8642d-115">Se questo parametro è escluso, il nome del file di configurazione di output viene codegen.config.</span><span class="sxs-lookup"><span data-stu-id="8642d-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="8642d-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="8642d-117">Includere un modello PnP-X nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8642d-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="8642d-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="8642d-119">Elenco delimitato da spazi dei file WSDL che devono essere elaborati da WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="8642d-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="8642d-120">Generazione del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="8642d-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="8642d-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8642d-121">Syntax</span></span>

<span data-ttu-id="8642d-122">**WSDCODEGEN.EXE** **/GenerateCode** **\[ /download \]** **\[ /GBC \]** **\[ outputroot:**_path_ *_\]_* **\[ /WriteAccess:**_Command_ *_\]_* *nomefileconfigurazione*</span><span class="sxs-lookup"><span data-stu-id="8642d-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="8642d-123">Parametri</span><span class="sxs-lookup"><span data-stu-id="8642d-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8642d-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="8642d-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="8642d-125">Indica a WsdCodeGen di generare codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="8642d-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="8642d-126">Questa è la modalità predefinita se non è specificata alcuna modalità.</span><span class="sxs-lookup"><span data-stu-id="8642d-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**</span><span class="sxs-lookup"><span data-stu-id="8642d-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="8642d-128">Scarica i documenti importati a cui fa riferimento il file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8642d-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="8642d-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8642d-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="8642d-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="8642d-131">Aggiunge commenti al codice sorgente che indica che il codice è stato generato.</span><span class="sxs-lookup"><span data-stu-id="8642d-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="8642d-132">Questi commenti hanno come prefisso la frase "generated by".</span><span class="sxs-lookup"><span data-stu-id="8642d-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="8642d-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8642d-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_percorso_</span><span class="sxs-lookup"><span data-stu-id="8642d-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="8642d-135">Percorso di output per i file generati.</span><span class="sxs-lookup"><span data-stu-id="8642d-135">The output location for generated files.</span></span> <span data-ttu-id="8642d-136">il *percorso* può essere un percorso assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="8642d-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="8642d-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8642d-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8642d-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/WriteAccess:**_comando_</span><span class="sxs-lookup"><span data-stu-id="8642d-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="8642d-139">Indica a WsdCodeGen di eseguire il comando specificato prima di modificare eventuali file esistenti sul disco.</span><span class="sxs-lookup"><span data-stu-id="8642d-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="8642d-140">I file di output identici a quelli sul disco non riceveranno questo comando né verranno scritti.</span><span class="sxs-lookup"><span data-stu-id="8642d-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="8642d-141">Se il comando contiene la sequenza " {0} ", questa sequenza verrà sostituita con il nome del file da modificare.</span><span class="sxs-lookup"><span data-stu-id="8642d-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="8642d-142">In caso contrario, il nome del file verrà aggiunto al comando.</span><span class="sxs-lookup"><span data-stu-id="8642d-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="8642d-143">Esempi:</span><span class="sxs-lookup"><span data-stu-id="8642d-143">Examples:</span></span>

<span data-ttu-id="8642d-144">**/WriteAccess: "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="8642d-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="8642d-145">**/WriteAccess: "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="8642d-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="8642d-146">**/WriteAccess: "copia {0} .. \\ backup \\ "**</span><span class="sxs-lookup"><span data-stu-id="8642d-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="8642d-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nomefileconfigurazione*</span><span class="sxs-lookup"><span data-stu-id="8642d-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="8642d-148">Nome del file di configurazione da elaborare prima di generare il codice.</span><span class="sxs-lookup"><span data-stu-id="8642d-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="8642d-149">Convenzioni di formattazione</span><span class="sxs-lookup"><span data-stu-id="8642d-149">Formatting Legend</span></span>



| <span data-ttu-id="8642d-150">Formato</span><span class="sxs-lookup"><span data-stu-id="8642d-150">Format</span></span>                                                                    | <span data-ttu-id="8642d-151">Significato</span><span class="sxs-lookup"><span data-stu-id="8642d-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8642d-152">*Corsivo*</span><span class="sxs-lookup"><span data-stu-id="8642d-152">*Italic*</span></span>                                                                  | <span data-ttu-id="8642d-153">Informazioni che l'utente deve fornire</span><span class="sxs-lookup"><span data-stu-id="8642d-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="8642d-154">**Grassetto**</span><span class="sxs-lookup"><span data-stu-id="8642d-154">**Bold**</span></span>                                                                  | <span data-ttu-id="8642d-155">Elementi che l'utente deve digitare esattamente come visualizzati</span><span class="sxs-lookup"><span data-stu-id="8642d-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="8642d-156">Tra parentesi quadre ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="8642d-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="8642d-157">Elementi facoltativi</span><span class="sxs-lookup"><span data-stu-id="8642d-157">Optional items</span></span>                                          |
| <span data-ttu-id="8642d-158">Tra parentesi graffe ( {} ); scelte separate da pipe ( \| ).</span><span class="sxs-lookup"><span data-stu-id="8642d-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="8642d-159">Esempio: {even \| Odd}</span><span class="sxs-lookup"><span data-stu-id="8642d-159">Example: {even\|odd}</span></span> | <span data-ttu-id="8642d-160">Set di opzioni da cui l'utente deve scegliere un solo</span><span class="sxs-lookup"><span data-stu-id="8642d-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8642d-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8642d-161">Requirements</span></span>



| <span data-ttu-id="8642d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="8642d-162">Requirement</span></span> | <span data-ttu-id="8642d-163">Valore</span><span class="sxs-lookup"><span data-stu-id="8642d-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8642d-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8642d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="8642d-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8642d-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8642d-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8642d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="8642d-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8642d-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8642d-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8642d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8642d-169">File di configurazione WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="8642d-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="8642d-170">Uso di WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="8642d-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




