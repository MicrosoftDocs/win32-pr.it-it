---
description: Il file VBScript WiLstPrd.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Lo script di esempio si connette a un oggetto del programma di installazione ed enumera i prodotti registrati e le informazioni sul prodotto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Elencare prodotti, proprietà, funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307247"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="61b6f-104">Elencare prodotti, proprietà, funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="61b6f-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="61b6f-105">Il file VBScript WiLstPrd.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="61b6f-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="61b6f-106">Lo script di esempio si connette a un oggetto del [**programma di installazione**](installer-object.md) ed enumera i prodotti registrati e le informazioni sul prodotto.</span><span class="sxs-lookup"><span data-stu-id="61b6f-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="61b6f-107">Questo esempio illustra l'uso di:</span><span class="sxs-lookup"><span data-stu-id="61b6f-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="61b6f-108">**Proprietà ProductInfo**</span><span class="sxs-lookup"><span data-stu-id="61b6f-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="61b6f-109">**Proprietà ProductState (oggetto Installer)**</span><span class="sxs-lookup"><span data-stu-id="61b6f-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="61b6f-110">**Products (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="61b6f-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="61b6f-111">**Proprietà features**</span><span class="sxs-lookup"><span data-stu-id="61b6f-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="61b6f-112">**Proprietà FeatureParent**</span><span class="sxs-lookup"><span data-stu-id="61b6f-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="61b6f-113">**Proprietà FeatureState**</span><span class="sxs-lookup"><span data-stu-id="61b6f-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="61b6f-114">**Components (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="61b6f-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="61b6f-115">**Proprietà ComponentClients**</span><span class="sxs-lookup"><span data-stu-id="61b6f-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="61b6f-116">**Proprietà ComponentPath**</span><span class="sxs-lookup"><span data-stu-id="61b6f-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="61b6f-117">**Metodo LastErrorRecord**</span><span class="sxs-lookup"><span data-stu-id="61b6f-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="61b6f-118">[**Metodo RegistryValue**](installer-registryvalue.md) dell' [ **oggetto Installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="61b6f-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="61b6f-119">Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="61b6f-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="61b6f-120">Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="61b6f-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="61b6f-121">La guida viene visualizzata se il primo argomento è/?</span><span class="sxs-lookup"><span data-stu-id="61b6f-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="61b6f-122">oppure se vengono specificati troppi argomenti.</span><span class="sxs-lookup"><span data-stu-id="61b6f-122">or if too few arguments are specified.</span></span> <span data-ttu-id="61b6f-123">Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] .</span><span class="sxs-lookup"><span data-stu-id="61b6f-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="61b6f-124">Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="61b6f-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="61b6f-125">**opzioni cscript WiLstPrd.vbs \[ Product Name \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="61b6f-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="61b6f-126">Specificare il nome prodotto senza distinzione tra maiuscole e minuscole o il GUID ID prodotto del prodotto installato o pubblicizzato.</span><span class="sxs-lookup"><span data-stu-id="61b6f-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="61b6f-127">Se non viene specificato alcun prodotto o opzione, il programma di installazione elenca tutti i prodotti installati o annunciati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="61b6f-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="61b6f-128">Si noti che queste opzioni non sono opzioni, pertanto non è necessario anteporre una barra (/) nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="61b6f-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="61b6f-129">Le opzioni seguenti possono essere combinate concatenando le lettere.</span><span class="sxs-lookup"><span data-stu-id="61b6f-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="61b6f-130">Ad esempio, "PC" per elencare le proprietà dei prodotti e i componenti installati.</span><span class="sxs-lookup"><span data-stu-id="61b6f-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="61b6f-131">Opzione</span><span class="sxs-lookup"><span data-stu-id="61b6f-131">Option</span></span>               | <span data-ttu-id="61b6f-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61b6f-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b6f-133">Nessuna opzione specificata</span><span class="sxs-lookup"><span data-stu-id="61b6f-133">no options specified</span></span> | <span data-ttu-id="61b6f-134">Elenca le proprietà dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="61b6f-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="61b6f-135">p</span><span class="sxs-lookup"><span data-stu-id="61b6f-135">p</span></span>                    | <span data-ttu-id="61b6f-136">Elenca le proprietà dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="61b6f-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="61b6f-137">f</span><span class="sxs-lookup"><span data-stu-id="61b6f-137">f</span></span>                    | <span data-ttu-id="61b6f-138">Elencare le funzionalità e gli Stati di installazione dei prodotti</span><span class="sxs-lookup"><span data-stu-id="61b6f-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="61b6f-139">c</span><span class="sxs-lookup"><span data-stu-id="61b6f-139">c</span></span>                    | <span data-ttu-id="61b6f-140">Elenca i componenti installati dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="61b6f-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="61b6f-141">d</span><span class="sxs-lookup"><span data-stu-id="61b6f-141">d</span></span>                    | <span data-ttu-id="61b6f-142">Elencare il valore in **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDLLs** per i file di chiave del componente Products.</span><span class="sxs-lookup"><span data-stu-id="61b6f-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="61b6f-143">Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) per ulteriori esempi di scripting.</span><span class="sxs-lookup"><span data-stu-id="61b6f-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="61b6f-144">Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="61b6f-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



