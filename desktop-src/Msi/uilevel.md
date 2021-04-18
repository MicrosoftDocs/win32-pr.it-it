---
description: Il programma di installazione imposta la proprietà UILevel sul livello dell'interfaccia utente.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Proprietà UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327918"
---
# <a name="uilevel-property"></a><span data-ttu-id="34368-103">Proprietà UILevel</span><span class="sxs-lookup"><span data-stu-id="34368-103">UILevel property</span></span>

<span data-ttu-id="34368-104">Il programma di installazione imposta la proprietà **UILevel** sul livello dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="34368-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="34368-105">L'interfaccia utente interna è abilitata e impostata da [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="34368-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="34368-106">Questa proprietà è impostata su uno dei tipi di dati INSTALLUILEVEL seguenti.</span><span class="sxs-lookup"><span data-stu-id="34368-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="34368-107">INSTALLUILEVEL</span><span class="sxs-lookup"><span data-stu-id="34368-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="34368-108">Valore numerico</span><span class="sxs-lookup"><span data-stu-id="34368-108">Numeric value</span></span> | <span data-ttu-id="34368-109">Livello dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="34368-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="34368-110">INSTALLUILEVEL \_ None</span><span class="sxs-lookup"><span data-stu-id="34368-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="34368-111">2</span><span class="sxs-lookup"><span data-stu-id="34368-111">2</span></span>             | <span data-ttu-id="34368-112">Installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="34368-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="34368-113">INSTALLUILEVEL \_ Basic</span><span class="sxs-lookup"><span data-stu-id="34368-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="34368-114">3</span><span class="sxs-lookup"><span data-stu-id="34368-114">3</span></span>             | <span data-ttu-id="34368-115">Semplice gestione degli errori e dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="34368-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="34368-116">INSTALLUILEVEL \_ ridotto</span><span class="sxs-lookup"><span data-stu-id="34368-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="34368-117">4</span><span class="sxs-lookup"><span data-stu-id="34368-117">4</span></span>             | <span data-ttu-id="34368-118">Interfaccia utente creata, finestre di dialogo della procedura guidata eliminati.</span><span class="sxs-lookup"><span data-stu-id="34368-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="34368-119">INSTALLUILEVEL \_ completo</span><span class="sxs-lookup"><span data-stu-id="34368-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="34368-120">5</span><span class="sxs-lookup"><span data-stu-id="34368-120">5</span></span>             | <span data-ttu-id="34368-121">Interfaccia utente creata con procedure guidate, stato, errori.</span><span class="sxs-lookup"><span data-stu-id="34368-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="34368-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34368-122">Requirements</span></span>



| <span data-ttu-id="34368-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="34368-123">Requirement</span></span> | <span data-ttu-id="34368-124">Valore</span><span class="sxs-lookup"><span data-stu-id="34368-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34368-125">Versione</span><span class="sxs-lookup"><span data-stu-id="34368-125">Version</span></span><br/> | <span data-ttu-id="34368-126">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34368-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34368-127">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34368-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34368-128">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34368-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="34368-129">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="34368-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34368-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34368-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34368-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34368-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="34368-132">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="34368-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="34368-133">Determinazione del livello dell'interfaccia utente da un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="34368-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




