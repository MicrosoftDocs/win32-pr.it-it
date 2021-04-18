---
description: La proprietà EXECUTEMODE specifica il modo in cui il programma di installazione esegue gli aggiornamenti del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Proprietà EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333782"
---
# <a name="executemode-property"></a><span data-ttu-id="0dd56-103">Proprietà EXECUTEMODE</span><span class="sxs-lookup"><span data-stu-id="0dd56-103">EXECUTEMODE property</span></span>

<span data-ttu-id="0dd56-104">La proprietà **EXECUTEMODE** specifica il modo in cui il programma di installazione esegue gli aggiornamenti del sistema.</span><span class="sxs-lookup"><span data-stu-id="0dd56-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="0dd56-105">Questa proprietà può essere utile quando è necessario eseguire un'installazione senza modificare effettivamente il sistema.</span><span class="sxs-lookup"><span data-stu-id="0dd56-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="0dd56-106">La proprietà può essere impostata su None per disabilitare le operazioni di aggiornamento, ad esempio l'installazione di file e i valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dd56-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="0dd56-107">Questa proprietà può avere uno dei due valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0dd56-107">This property can have one of the following two values.</span></span> <span data-ttu-id="0dd56-108">Il programma di installazione esamina solo la prima lettera del valore e non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0dd56-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="0dd56-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno</span><span class="sxs-lookup"><span data-stu-id="0dd56-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="0dd56-110">Non viene apportata alcuna modifica al sistema.</span><span class="sxs-lookup"><span data-stu-id="0dd56-110">No changes are made to the system.</span></span> <span data-ttu-id="0dd56-111">Il programma di installazione esegue l'interfaccia utente e quindi esegue una query sul database.</span><span class="sxs-lookup"><span data-stu-id="0dd56-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="0dd56-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span><span class="sxs-lookup"><span data-stu-id="0dd56-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="0dd56-113">Tutte le modifiche apportate al sistema vengono eseguite tramite l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="0dd56-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="0dd56-114">Si tratta della modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="0dd56-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="0dd56-115">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0dd56-115">Default Value</span></span>

<span data-ttu-id="0dd56-116">Se questa proprietà non è definita, il valore predefinito della modalità di esecuzione è script.</span><span class="sxs-lookup"><span data-stu-id="0dd56-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd56-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd56-117">Requirements</span></span>



| <span data-ttu-id="0dd56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd56-118">Requirement</span></span> | <span data-ttu-id="0dd56-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd56-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd56-120">Versione</span><span class="sxs-lookup"><span data-stu-id="0dd56-120">Version</span></span><br/> | <span data-ttu-id="0dd56-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0dd56-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0dd56-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0dd56-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0dd56-123">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0dd56-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0dd56-124">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0dd56-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0dd56-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd56-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0dd56-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




