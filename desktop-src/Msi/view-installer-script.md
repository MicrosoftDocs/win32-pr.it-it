---
description: Il file VBScript WiLstScr.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio illustra il Visualizzatore di script Windows Installer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Visualizza script del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308664"
---
# <a name="view-installer-script"></a><span data-ttu-id="ae0db-104">Visualizza script del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ae0db-104">View Installer Script</span></span>

<span data-ttu-id="ae0db-105">Il file VBScript WiLstScr.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ae0db-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ae0db-106">Questo script di esempio illustra il Visualizzatore di script Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ae0db-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="ae0db-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="ae0db-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="ae0db-108">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="ae0db-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="ae0db-109">Metodo [**LastErrorRecord**](installer-lasterrorrecord.md) dell'oggetto [**Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="ae0db-110">Metodo [**OpenView**](database-openview.md) dell'oggetto di [**database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="ae0db-111">Metodo [**Fetch**](view-fetch.md) dell'oggetto [**View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="ae0db-112">Metodo [**FormatText**](record-formattext.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="ae0db-113">Proprietà [**FieldCount**](record-fieldcount.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="ae0db-114">Proprietà [**StringData**](record-stringdata.md) dell'oggetto [**record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae0db-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="ae0db-115">\_Tabella transformview</span><span class="sxs-lookup"><span data-stu-id="ae0db-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="ae0db-116">Per usare questo esempio è necessaria la versione CScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="ae0db-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="ae0db-117">Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="ae0db-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="ae0db-118">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="ae0db-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ae0db-119">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="ae0db-119">or if too few arguments are specified.</span></span> <span data-ttu-id="ae0db-120">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="ae0db-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ae0db-121">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ae0db-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ae0db-122">**cscript WiLstScr.vbs** *\[ percorso Windows Installer script \] di esecuzione*</span><span class="sxs-lookup"><span data-stu-id="ae0db-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="ae0db-123">Specificare il percorso dello script di esecuzione del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ae0db-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="ae0db-124">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ae0db-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ae0db-125">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ae0db-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



