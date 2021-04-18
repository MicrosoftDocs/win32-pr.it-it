---
description: Arresta l'agente di raccolta. Se l'agente di raccolta è in esecuzione come servizio, l'arresto del servizio è l'approccio migliore.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Metodo Shutdown della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304449"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="9f58c-104">Metodo Shutdown della classe Control</span><span class="sxs-lookup"><span data-stu-id="9f58c-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="9f58c-105">Arresta l'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="9f58c-105">Stops the collector.</span></span> <span data-ttu-id="9f58c-106">Se l'agente di raccolta è in esecuzione come servizio, l'arresto del servizio è l'approccio migliore.</span><span class="sxs-lookup"><span data-stu-id="9f58c-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f58c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f58c-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="9f58c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f58c-108">Parameters</span></span>

<span data-ttu-id="9f58c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f58c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f58c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f58c-110">Return value</span></span>

<span data-ttu-id="9f58c-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9f58c-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f58c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f58c-112">Requirements</span></span>



| <span data-ttu-id="9f58c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f58c-113">Requirement</span></span> | <span data-ttu-id="9f58c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9f58c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f58c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f58c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9f58c-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9f58c-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f58c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f58c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9f58c-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9f58c-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="9f58c-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f58c-119">Namespace</span></span><br/>                | <span data-ttu-id="9f58c-120">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="9f58c-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="9f58c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="9f58c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f58c-122"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f58c-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f58c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9f58c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f58c-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f58c-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9f58c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f58c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f58c-126">**Control**</span><span class="sxs-lookup"><span data-stu-id="9f58c-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




