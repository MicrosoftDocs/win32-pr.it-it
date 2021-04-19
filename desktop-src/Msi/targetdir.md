---
description: La proprietà TARGETDIR specifica la directory di destinazione radice per l'installazione.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Proprietà TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329952"
---
# <a name="targetdir-property"></a><span data-ttu-id="8be58-103">Proprietà TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="8be58-103">TARGETDIR property</span></span>

<span data-ttu-id="8be58-104">La proprietà **targetdir** specifica la directory di destinazione radice per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8be58-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="8be58-105">**Targetdir** deve essere il nome di una radice nella tabella [directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8be58-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="8be58-106">Può essere presente una sola directory di destinazione radice.</span><span class="sxs-lookup"><span data-stu-id="8be58-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="8be58-107">Durante un' [installazione amministrativa](administrative-installation.md) questa proprietà specifica il percorso in cui copiare il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="8be58-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="8be58-108">Durante un'installazione non amministrativa questa proprietà specifica la directory di destinazione radice.</span><span class="sxs-lookup"><span data-stu-id="8be58-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="8be58-109">Per specificare la directory di destinazione radice, impostare la colonna directory della tabella directory sulla proprietà **targetdir** e la colonna DefaultDir sulla proprietà [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="8be58-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="8be58-110">Se la proprietà **targetdir** è definita, la directory di destinazione viene risolta nel valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8be58-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="8be58-111">Se la proprietà **targetdir** è indefinita, per risolvere il percorso viene utilizzata la proprietà [**ROOTDRIVE**](rootdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="8be58-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="8be58-112">Per ulteriori informazioni sull'utilizzo della proprietà **targetdir** , vedere [utilizzo della tabella directory](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="8be58-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="8be58-113">Si noti che il valore della proprietà **targetdir** viene in genere impostato dalla riga di comando o tramite un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="8be58-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="8be58-114">L'impostazione di **targetdir** tramite la creazione di un percorso nella [tabella delle proprietà](property-table.md) non è consigliata perché i computer sono diversi nella configurazione dell'unità locale.</span><span class="sxs-lookup"><span data-stu-id="8be58-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="8be58-115">Per ulteriori informazioni su come modificare TARGETDIR durante un'installazione, vedere [modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="8be58-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="8be58-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8be58-116">Requirements</span></span>



| <span data-ttu-id="8be58-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be58-117">Requirement</span></span> | <span data-ttu-id="8be58-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8be58-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be58-119">Versione</span><span class="sxs-lookup"><span data-stu-id="8be58-119">Version</span></span><br/> | <span data-ttu-id="8be58-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8be58-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8be58-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8be58-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8be58-122">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8be58-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8be58-123">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8be58-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8be58-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8be58-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be58-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8be58-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




