---
description: Il file VBScript WiToAnsi.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per riscrivere un file di testo Unicode come file di testo ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiare un file Unicode in un file ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882737"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="0dd73-104">Copiare un file Unicode in un file ANSI</span><span class="sxs-lookup"><span data-stu-id="0dd73-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="0dd73-105">Il file VBScript WiToAnsi.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0dd73-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="0dd73-106">In questo esempio viene illustrato come utilizzare lo script per riscrivere un file di testo Unicode come file di testo ANSI.</span><span class="sxs-lookup"><span data-stu-id="0dd73-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="0dd73-107">Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="0dd73-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="0dd73-108">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="0dd73-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="0dd73-109">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="0dd73-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="0dd73-110">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="0dd73-110">or if too few arguments are specified.</span></span> <span data-ttu-id="0dd73-111">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="0dd73-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="0dd73-112">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0dd73-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="0dd73-113">**cscript WiToAnsi.vbs \[ percorso del file Unicode \] \[ al file ANSI\]**</span><span class="sxs-lookup"><span data-stu-id="0dd73-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="0dd73-114">Specificare il file di testo Unicode da convertire.</span><span class="sxs-lookup"><span data-stu-id="0dd73-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="0dd73-115">Specificare il file di testo ANSI da creare.</span><span class="sxs-lookup"><span data-stu-id="0dd73-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="0dd73-116">Se non viene specificato alcun file ANSI, il file Unicode viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="0dd73-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="0dd73-117">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0dd73-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="0dd73-118">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0dd73-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



