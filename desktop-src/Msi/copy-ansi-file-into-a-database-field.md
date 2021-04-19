---
description: Il file di esempio di codice VBScript WiTextIn.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copia il file ANSI in un campo di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313816"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="259b4-103">Copia il file ANSI in un campo di database</span><span class="sxs-lookup"><span data-stu-id="259b4-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="259b4-104">Il file di esempio di codice VBScript WiTextIn.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="259b4-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="259b4-105">Nell'esempio viene illustrato come è possibile utilizzare uno script per copiare un file in un campo di testo di un database di Windows Installer e viene illustrata l'elaborazione dei dati della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="259b4-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="259b4-106">L'esempio di codice mostra anche quanto segue:</span><span class="sxs-lookup"><span data-stu-id="259b4-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="259b4-107">[**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md) e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="259b4-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="259b4-108">[**Metodo OpenView**](database-openview.md), [**metodo commit**](database-commit.md)e [**Proprietà PrimaryKeys**](database-primarykeys.md) dell' [**oggetto di database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="259b4-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="259b4-109">[**Metodo fetch**](view-fetch.md) e [**metodo modify**](view-modify.md) dell' [**oggetto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="259b4-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="259b4-110">[**Proprietà StringData**](record-stringdata.md) e [**Metodo ReadStream**](record-readstream.md) dell' [**oggetto record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="259b4-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="259b4-111">Per utilizzare l'esempio di codice è necessario disporre della versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="259b4-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="259b4-112">**Per utilizzare CScript.exe per eseguire l'esempio**</span><span class="sxs-lookup"><span data-stu-id="259b4-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="259b4-113">Al prompt dei comandi digitare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="259b4-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="259b4-114">**cscript WiTextIn.vbs \[ percorso del nome della tabella del database \] \[ nome della \] \[ colonna valori di chiave primaria \] \[ percorso del \] \[ file\]**</span><span class="sxs-lookup"><span data-stu-id="259b4-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="259b4-115">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="259b4-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="259b4-116">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="259b4-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="259b4-117">**Per reindirizzare l'output a un file**</span><span class="sxs-lookup"><span data-stu-id="259b4-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="259b4-118">Terminare la riga di comando con il seguente **> il \[ percorso del file vbs \] . T**</span><span class="sxs-lookup"><span data-stu-id="259b4-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="259b4-119">L'esempio restituisce un valore pari a 0 (zero) per esito positivo, 1 (uno) se la guida viene richiamata e 2 (due) se lo script non riesce.</span><span class="sxs-lookup"><span data-stu-id="259b4-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="259b4-120">L'elenco seguente identifica gli elementi che è necessario specificare:</span><span class="sxs-lookup"><span data-stu-id="259b4-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="259b4-121">Consente di specificare il percorso del database di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="259b4-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="259b4-122">Consente di specificare il nome della tabella di database.</span><span class="sxs-lookup"><span data-stu-id="259b4-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="259b4-123">Specificare tutti i valori di chiave primaria per la riga, nell'ordine e concatenati con i due punti.</span><span class="sxs-lookup"><span data-stu-id="259b4-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="259b4-124">Specificare un nome di colonna che non sia una colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="259b4-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="259b4-125">Si tratta della colonna a cui si desidera ricevere i dati.</span><span class="sxs-lookup"><span data-stu-id="259b4-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="259b4-126">Specificare il percorso del file di testo da copiare.</span><span class="sxs-lookup"><span data-stu-id="259b4-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="259b4-127">Se l'ultimo argomento viene omesso, viene visualizzato il valore corrente nel campo.</span><span class="sxs-lookup"><span data-stu-id="259b4-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="259b4-128">Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="259b4-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="259b4-129">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="259b4-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



