---
description: La proprietà UILevel dell'oggetto Installer è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da utilizzare per l'apertura e l'elaborazione di pacchetti successivi nello spazio di processo corrente.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Proprietà Installer. UILevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333165"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="e44d2-103">Proprietà Installer. UILevel</span><span class="sxs-lookup"><span data-stu-id="e44d2-103">Installer.UILevel property</span></span>

<span data-ttu-id="e44d2-104">La proprietà **UILevel** dell'oggetto [**Installer**](installer-object.md) è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da utilizzare per l'apertura e l'elaborazione di pacchetti successivi nello spazio di processo corrente.</span><span class="sxs-lookup"><span data-stu-id="e44d2-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="e44d2-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e44d2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44d2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e44d2-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="e44d2-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e44d2-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e44d2-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e44d2-108">Remarks</span></span>



| <span data-ttu-id="e44d2-109">Livello dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e44d2-109">User interface level</span></span>   | <span data-ttu-id="e44d2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e44d2-110">Value</span></span> | <span data-ttu-id="e44d2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e44d2-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44d2-112">msiUILevelNoChange</span><span class="sxs-lookup"><span data-stu-id="e44d2-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="e44d2-113">0</span><span class="sxs-lookup"><span data-stu-id="e44d2-113">0</span></span>     | <span data-ttu-id="e44d2-114">Non modifica il livello dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e44d2-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="e44d2-115">msiUILevelDefault</span><span class="sxs-lookup"><span data-stu-id="e44d2-115">msiUILevelDefault</span></span>      | <span data-ttu-id="e44d2-116">1</span><span class="sxs-lookup"><span data-stu-id="e44d2-116">1</span></span>     | <span data-ttu-id="e44d2-117">Usa il livello di interfaccia utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="e44d2-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="e44d2-118">msiUILevelNone</span><span class="sxs-lookup"><span data-stu-id="e44d2-118">msiUILevelNone</span></span>         | <span data-ttu-id="e44d2-119">2</span><span class="sxs-lookup"><span data-stu-id="e44d2-119">2</span></span>     | <span data-ttu-id="e44d2-120">Installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="e44d2-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="e44d2-121">msiUILevelBasic</span><span class="sxs-lookup"><span data-stu-id="e44d2-121">msiUILevelBasic</span></span>        | <span data-ttu-id="e44d2-122">3</span><span class="sxs-lookup"><span data-stu-id="e44d2-122">3</span></span>     | <span data-ttu-id="e44d2-123">Semplice gestione degli errori e dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e44d2-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="e44d2-124">msiUILevelReduced</span><span class="sxs-lookup"><span data-stu-id="e44d2-124">msiUILevelReduced</span></span>      | <span data-ttu-id="e44d2-125">4</span><span class="sxs-lookup"><span data-stu-id="e44d2-125">4</span></span>     | <span data-ttu-id="e44d2-126">Finestre di dialogo dell'interfaccia utente e della procedura guidata Create ed eliminati.</span><span class="sxs-lookup"><span data-stu-id="e44d2-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="e44d2-127">msiUILevelFull</span><span class="sxs-lookup"><span data-stu-id="e44d2-127">msiUILevelFull</span></span>         | <span data-ttu-id="e44d2-128">5</span><span class="sxs-lookup"><span data-stu-id="e44d2-128">5</span></span>     | <span data-ttu-id="e44d2-129">Interfaccia utente creata con procedure guidate, stato ed errori.</span><span class="sxs-lookup"><span data-stu-id="e44d2-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="e44d2-130">msiUILevelHideCancel</span><span class="sxs-lookup"><span data-stu-id="e44d2-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="e44d2-131">32</span><span class="sxs-lookup"><span data-stu-id="e44d2-131">32</span></span>    | <span data-ttu-id="e44d2-132">Se combinato con il valore msiUILevelBasic, il programma di installazione Mostra le finestre di dialogo di stato ma non visualizza un pulsante **Annulla** nella finestra di dialogo per impedire agli utenti di annullare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e44d2-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="e44d2-133">msiUILevelProgressOnly</span><span class="sxs-lookup"><span data-stu-id="e44d2-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="e44d2-134">64</span><span class="sxs-lookup"><span data-stu-id="e44d2-134">64</span></span>    | <span data-ttu-id="e44d2-135">Se combinato con il valore msiUILevelBasic, nel programma di installazione vengono visualizzate le finestre di dialogo di stato ma non vengono visualizzate finestre di dialogo modali o finestre di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="e44d2-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="e44d2-136">msiUILevelEndDialog</span><span class="sxs-lookup"><span data-stu-id="e44d2-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="e44d2-137">128</span><span class="sxs-lookup"><span data-stu-id="e44d2-137">128</span></span>   | <span data-ttu-id="e44d2-138">Se combinato con qualsiasi valore precedente, il programma di installazione visualizza una finestra di dialogo modale alla fine di una corretta installazione o se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="e44d2-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="e44d2-139">Se l'utente Annulla, non verrà visualizzata alcuna finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e44d2-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="e44d2-140">Vedere anche [determinazione del livello dell'interfaccia utente da un'azione personalizzata](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="e44d2-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e44d2-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e44d2-141">Requirements</span></span>



| <span data-ttu-id="e44d2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="e44d2-142">Requirement</span></span> | <span data-ttu-id="e44d2-143">Valore</span><span class="sxs-lookup"><span data-stu-id="e44d2-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44d2-144">Versione</span><span class="sxs-lookup"><span data-stu-id="e44d2-144">Version</span></span><br/> | <span data-ttu-id="e44d2-145">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e44d2-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e44d2-146">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e44d2-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e44d2-147">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e44d2-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e44d2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e44d2-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="e44d2-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e44d2-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e44d2-150">IID</span><span class="sxs-lookup"><span data-stu-id="e44d2-150">IID</span></span><br/>     | <span data-ttu-id="e44d2-151">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e44d2-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




