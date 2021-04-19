---
description: La proprietà PROMPTROLLBACKCOST specifica l'azione eseguita dal programma di installazione se le funzionalità di installazione rollback sono abilitate e lo spazio su disco è insufficiente per completare l'installazione. I valori possibili di PROMPTROLLBACKCOST sono i seguenti. ValueActionPDisplay una finestra di dialogo in cui viene chiesto se continuare senza eseguire il rollback. DDisable rollback e continua senza richiedere l'intervento dell'utente. FFail con il messaggio di errore di spazio su disco insufficiente.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Proprietà PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332607"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="b1251-103">Proprietà PROMPTROLLBACKCOST</span><span class="sxs-lookup"><span data-stu-id="b1251-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="b1251-104">La proprietà **PROMPTROLLBACKCOST** specifica l'azione eseguita dal programma di installazione se le funzionalità di [installazione rollback](rollback-installation.md) sono abilitate e lo spazio su disco è insufficiente per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b1251-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="b1251-105">I valori possibili di **PROMPTROLLBACKCOST** sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1251-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="b1251-106">Valore</span><span class="sxs-lookup"><span data-stu-id="b1251-106">Value</span></span> | <span data-ttu-id="b1251-107">Azione</span><span class="sxs-lookup"><span data-stu-id="b1251-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="b1251-108">P</span><span class="sxs-lookup"><span data-stu-id="b1251-108">P</span></span>     | <span data-ttu-id="b1251-109">Consente di visualizzare una finestra di dialogo in cui viene chiesto se continuare senza rollback.</span><span class="sxs-lookup"><span data-stu-id="b1251-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="b1251-110">D</span><span class="sxs-lookup"><span data-stu-id="b1251-110">D</span></span>     | <span data-ttu-id="b1251-111">Disabilitare il rollback e continuare senza richiedere l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b1251-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="b1251-112">F</span><span class="sxs-lookup"><span data-stu-id="b1251-112">F</span></span>     | <span data-ttu-id="b1251-113">Ha esito negativo con il messaggio di errore di spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b1251-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="b1251-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1251-114">Remarks</span></span>

<span data-ttu-id="b1251-115">Quando l'interfaccia utente viene eseguita a livello di base o senza interfaccia utente, il programma di installazione gestisce automaticamente tutta la logica di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="b1251-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="b1251-116">Quando l'interfaccia utente viene eseguita a livello completo, all'utente possono essere concesse opzioni aggiuntive, ad esempio la richiesta prima di procedere con un rollback, la disabilitazione del rollback o la continuazione senza rollback quando il disco è pieno.</span><span class="sxs-lookup"><span data-stu-id="b1251-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="b1251-117">Lo sviluppatore del pacchetto deve creare la sequenza della finestra di dialogo per fornire le scelte appropriate all'utente.</span><span class="sxs-lookup"><span data-stu-id="b1251-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="b1251-118">Gli elementi disponibili per eseguire questa operazione sono la proprietà [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) , [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) e la proprietà **PROMPTROLLBACKCOST** .</span><span class="sxs-lookup"><span data-stu-id="b1251-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1251-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1251-119">Requirements</span></span>



| <span data-ttu-id="b1251-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1251-120">Requirement</span></span> | <span data-ttu-id="b1251-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b1251-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1251-122">Versione</span><span class="sxs-lookup"><span data-stu-id="b1251-122">Version</span></span><br/> | <span data-ttu-id="b1251-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b1251-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b1251-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1251-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b1251-125">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1251-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b1251-126">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b1251-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1251-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1251-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1251-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1251-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




