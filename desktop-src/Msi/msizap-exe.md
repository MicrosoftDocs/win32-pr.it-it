---
description: Msizap.exe è un'utilità della riga di comando che rimuove tutte le informazioni Windows Installer per un prodotto o tutti i prodotti installati in un computer. I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049828"
---
# <a name="msizapexe"></a><span data-ttu-id="072b7-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="072b7-104">Msizap.exe</span></span>

<span data-ttu-id="072b7-105">Msizap.exe è un'utilità della riga di comando che rimuove tutte le informazioni Windows Installer per un prodotto o tutti i prodotti installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="072b7-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="072b7-106">I prodotti installati dal programma di installazione potrebbero non funzionare dopo l'uso di Msizap.</span><span class="sxs-lookup"><span data-stu-id="072b7-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="072b7-107">In Windows 2000 e Windows XP sono necessari privilegi amministrativi per usare Msizap.exe.</span><span class="sxs-lookup"><span data-stu-id="072b7-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="072b7-108">Questo strumento è disponibile solo nei [componenti Windows SDK per gli sviluppatori di Windows Installer](platform-sdk-components-for-windows-installer-developers.md) e non deve essere ridistribuito.</span><span class="sxs-lookup"><span data-stu-id="072b7-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="072b7-109">Utilizzare la versione recente di Msizap.exe (versione 3.1.4000.2726 o successiva) disponibile nei componenti Windows SDK per Windows Installer sviluppatori per Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="072b7-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="072b7-110">Versioni minori di Msizap.exe possono rimuovere informazioni su tutti gli aggiornamenti applicati ad altre applicazioni nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="072b7-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="072b7-111">Se queste informazioni vengono rimosse, potrebbe essere necessario rimuovere e reinstallare le altre applicazioni per ricevere ulteriori aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="072b7-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="072b7-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="072b7-112">Syntax</span></span>

<span data-ttu-id="072b7-113">**Msizap T**_\[ WA! \] {Codice prodotto}_</span><span class="sxs-lookup"><span data-stu-id="072b7-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="072b7-114">**Msizap T**_\[ WA! \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="072b7-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="072b7-115">\**\* \*\*\* Msizap \[ WA! \]* **ALLPRODUCTS**</span><span class="sxs-lookup"><span data-stu-id="072b7-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="072b7-116">**Msizap PWSA?**</span><span class="sxs-lookup"><span data-stu-id="072b7-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="072b7-117">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="072b7-117">Command Line Options</span></span>

<span data-ttu-id="072b7-118">Msizap.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="072b7-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="072b7-119">Opzione</span><span class="sxs-lookup"><span data-stu-id="072b7-119">Option</span></span> | <span data-ttu-id="072b7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="072b7-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="072b7-121">Rimuove tutti i Windows Installer cartelle e le chiavi del registro di sistema, regola i conteggi delle DLL condivise e arresta Windows Installer servizio.</span><span class="sxs-lookup"><span data-stu-id="072b7-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="072b7-122">Rimuove anche la chiave di In-Progress e le informazioni di rollback.</span><span class="sxs-lookup"><span data-stu-id="072b7-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="072b7-123">a</span><span class="sxs-lookup"><span data-stu-id="072b7-123">a</span></span>      | <span data-ttu-id="072b7-124">Modifica solo gli ACL per il controllo completo dell'amministratore per qualsiasi rimozione specificata.</span><span class="sxs-lookup"><span data-stu-id="072b7-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="072b7-125">g</span><span class="sxs-lookup"><span data-stu-id="072b7-125">g</span></span>      | <span data-ttu-id="072b7-126">Per tutti gli utenti, rimuove tutti i file di dati Windows Installer memorizzati nella cache che sono stati orfani.</span><span class="sxs-lookup"><span data-stu-id="072b7-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="072b7-127">p</span><span class="sxs-lookup"><span data-stu-id="072b7-127">p</span></span>      | <span data-ttu-id="072b7-128">Rimuove la chiave In-Progress.</span><span class="sxs-lookup"><span data-stu-id="072b7-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="072b7-129">s</span><span class="sxs-lookup"><span data-stu-id="072b7-129">s</span></span>      | <span data-ttu-id="072b7-130">Rimuove le informazioni di rollback.</span><span class="sxs-lookup"><span data-stu-id="072b7-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="072b7-131">u</span><span class="sxs-lookup"><span data-stu-id="072b7-131">t</span></span>      | <span data-ttu-id="072b7-132">Rimuove tutte le informazioni per il codice prodotto specificato.</span><span class="sxs-lookup"><span data-stu-id="072b7-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="072b7-133">Quando si usa questa opzione, racchiudere il codice del prodotto tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="072b7-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="072b7-134">Questa opzione può essere utilizzata con il percorso completo del file con estensione msi o con il codice prodotto.</span><span class="sxs-lookup"><span data-stu-id="072b7-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="072b7-135">w</span><span class="sxs-lookup"><span data-stu-id="072b7-135">w</span></span>      | <span data-ttu-id="072b7-136">Rimuove Windows Installer informazioni per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="072b7-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="072b7-137">Quando questa opzione non è impostata, vengono rimosse solo le informazioni relative all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="072b7-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="072b7-138">Per usare questa opzione è necessario che il profilo dell'utente sia caricato in modo che l'hive del registro di sistema per utente sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="072b7-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="072b7-139">?</span><span class="sxs-lookup"><span data-stu-id="072b7-139">?</span></span>      | <span data-ttu-id="072b7-140">Guida dettagliata.</span><span class="sxs-lookup"><span data-stu-id="072b7-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="072b7-141">!</span><span class="sxs-lookup"><span data-stu-id="072b7-141">!</span></span>      | <span data-ttu-id="072b7-142">Forza una risposta "Yes" a qualsiasi richiesta.</span><span class="sxs-lookup"><span data-stu-id="072b7-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="072b7-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="072b7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="072b7-144">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="072b7-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



