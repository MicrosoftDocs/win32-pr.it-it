---
description: Il file VBScript WiLangID.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gestisci lingua e tabella codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318279"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="6acc5-103">Gestisci lingua e tabella codici</span><span class="sxs-lookup"><span data-stu-id="6acc5-103">Manage Language and Codepage</span></span>

<span data-ttu-id="6acc5-104">Il file VBScript WiLangID.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="6acc5-105">In questo esempio viene illustrato come utilizzare lo script per accedere alle informazioni sulla lingua e alla tabella codici di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6acc5-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="6acc5-106">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md) e alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="6acc5-107">Nell'esempio viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="6acc5-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="6acc5-108">**Metodo OpenDatabase (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="6acc5-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="6acc5-109">**Metodo CreaRecord**</span><span class="sxs-lookup"><span data-stu-id="6acc5-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="6acc5-110">[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="6acc5-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="6acc5-111">**OpenView (metodo)**</span><span class="sxs-lookup"><span data-stu-id="6acc5-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="6acc5-112">[**Proprietà SummaryInformation (oggetto di database)**](database-summaryinformation.md) dell' [ **oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="6acc5-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="6acc5-113">Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="6acc5-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="6acc5-114">Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="6acc5-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="6acc5-115">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="6acc5-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="6acc5-116">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="6acc5-116">or if too few arguments are specified.</span></span> <span data-ttu-id="6acc5-117">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] .</span><span class="sxs-lookup"><span data-stu-id="6acc5-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="6acc5-118">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6acc5-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="6acc5-119">**valore della \[ \] \[ parola chiave database \] cscript WiLangID.vbs Path \[\]**</span><span class="sxs-lookup"><span data-stu-id="6acc5-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="6acc5-120">Consente di specificare il percorso del database di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6acc5-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="6acc5-121">Per modificare un valore, specificare una delle parole chiave seguenti seguite dal nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="6acc5-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="6acc5-122">Se non viene specificato alcun valore, l'esempio restituisce il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="6acc5-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="6acc5-123">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="6acc5-123">Keyword</span></span>      | <span data-ttu-id="6acc5-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6acc5-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acc5-125">**Pacchetto**</span><span class="sxs-lookup"><span data-stu-id="6acc5-125">**Package**</span></span>  | <span data-ttu-id="6acc5-126">Versioni del linguaggio supportate dal database.</span><span class="sxs-lookup"><span data-stu-id="6acc5-126">The language versions supported by the database.</span></span> <span data-ttu-id="6acc5-127">Per informazioni, vedere Proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="6acc5-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="6acc5-128">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="6acc5-128">**Product**</span></span>  | <span data-ttu-id="6acc5-129">Lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database.</span><span class="sxs-lookup"><span data-stu-id="6acc5-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="6acc5-130">Per informazioni, vedere proprietà [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="6acc5-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="6acc5-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="6acc5-131">**Codepage**</span></span> | <span data-ttu-id="6acc5-132">Tabella codici ANSI singola per il pool di stringhe.</span><span class="sxs-lookup"><span data-stu-id="6acc5-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="6acc5-133">Per informazioni, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="6acc5-134">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="6acc5-135">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="6acc5-136">Per ulteriori informazioni, vedere la pagina relativa alla [determinazione della tabella codici](determining-an-installation-database-s-code-page.md) di un database di installazione e [l'impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="6acc5-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



