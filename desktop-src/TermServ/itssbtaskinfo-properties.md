---
title: Proprietà di ITsSbTaskInfo
description: L'interfaccia ITsSbTaskInfo espone le proprietà seguenti.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718283"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="ea449-103">Proprietà di ITsSbTaskInfo</span><span class="sxs-lookup"><span data-stu-id="ea449-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="ea449-104">L'interfaccia [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea449-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ea449-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ea449-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ea449-106">**Proprietà di contesto**</span><span class="sxs-lookup"><span data-stu-id="ea449-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="ea449-107">Recupera i byte del contesto associati all'attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-108">**Proprietà scadenza**</span><span class="sxs-lookup"><span data-stu-id="ea449-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="ea449-109">Recupera l'ora in cui l'attività deve essere avviata.</span><span class="sxs-lookup"><span data-stu-id="ea449-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="ea449-110">Viene usato per assegnare priorità alle patch.</span><span class="sxs-lookup"><span data-stu-id="ea449-110">This is used to prioritize patches.</span></span> <span data-ttu-id="ea449-111">Per prima cosa viene avviata la patch con la prima scadenza.</span><span class="sxs-lookup"><span data-stu-id="ea449-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-112">**Proprietà EndTime**</span><span class="sxs-lookup"><span data-stu-id="ea449-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="ea449-113">Recupera l'ultima volta che l'agente attività è in grado di avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-114">**Proprietà Identificatore**</span><span class="sxs-lookup"><span data-stu-id="ea449-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="ea449-115">Recupera un GUID utilizzato come identificatore univoco da parte dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-116">**proprietà Label**</span><span class="sxs-lookup"><span data-stu-id="ea449-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="ea449-117">Recupera l'etichetta che descrive lo scopo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-118">**Proprietà del plug-in**</span><span class="sxs-lookup"><span data-stu-id="ea449-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="ea449-119">Recupera il nome visualizzato dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-120">**StartTime (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="ea449-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="ea449-121">Recupera la prima volta che l'agente attività è in grado di avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-122">**Status (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="ea449-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="ea449-123">Recupera un valore di enumerazione [**\_ \_ dello stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ea449-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="ea449-124">**Proprietà TargetId**</span><span class="sxs-lookup"><span data-stu-id="ea449-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="ea449-125">Recupera l'identificatore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ea449-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




