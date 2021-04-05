---
description: ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della tabella IniFile esista nel pacchetto di Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884330"
---
# <a name="ice88"></a><span data-ttu-id="b6852-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="b6852-103">ICE88</span></span>

<span data-ttu-id="b6852-104">ICE88 verifica che la directory a cui viene fatto riferimento nella colonna DirProperty della [tabella inifile](inifile-table.md) esista nel pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b6852-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="b6852-105">ICE88 genera un avviso se il valore DirProperty non rappresenta una proprietà nella directory, AppSearch, o nelle tabelle delle proprietà, in determinate [proprietà della cartella di sistema](property-reference.md)o in una proprietà impostata da un'azione personalizzata di tipo 51.</span><span class="sxs-lookup"><span data-stu-id="b6852-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="b6852-106">ICE88 analizza le seguenti tabelle e proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6852-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="b6852-107">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="b6852-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="b6852-108">Tabella AppSearch</span><span class="sxs-lookup"><span data-stu-id="b6852-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="b6852-109">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b6852-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="b6852-110">[Tabella CustomAction](customaction-table.md) , in cui l'azione personalizzata è un [tipo di azione personalizzata 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="b6852-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="b6852-111">**Proprietà ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="b6852-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="b6852-112">**Proprietà CommonFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="b6852-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="b6852-113">**Proprietà SystemFolder**</span><span class="sxs-lookup"><span data-stu-id="b6852-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="b6852-114">**Proprietà ProgramFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="b6852-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="b6852-115">**Proprietà CommonFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="b6852-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="b6852-116">**Proprietà System64Folder**</span><span class="sxs-lookup"><span data-stu-id="b6852-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="b6852-117">Risultato</span><span class="sxs-lookup"><span data-stu-id="b6852-117">Result</span></span>

<span data-ttu-id="b6852-118">ICE88 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="b6852-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="b6852-119">Avviso di ICE88</span><span class="sxs-lookup"><span data-stu-id="b6852-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="b6852-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6852-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6852-121">Nella voce della tabella IniFile (IniFile =) \[ 3 \] DirProperty = \[ 1 \] non è disponibile nelle tabelle directory/Property/AppSearch/CA-Type51 e non è una delle proprietà del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b6852-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="b6852-122">Per ogni record nella tabella IniFile, ICE88 legge il valore nella colonna DirProperty.</span><span class="sxs-lookup"><span data-stu-id="b6852-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="b6852-123">ICE88 analizza il valore nella tabella di [directory](directory-table.md), nella tabella [AppSearch](appsearch-table.md)e nella [tabella delle proprietà](property-table.md) e analizza anche l'elenco delle proprietà impostate dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b6852-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="b6852-124">ICE88 Invia questo avviso se il valore non è stato trovato nell'analisi.</span><span class="sxs-lookup"><span data-stu-id="b6852-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b6852-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6852-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6852-126">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b6852-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



