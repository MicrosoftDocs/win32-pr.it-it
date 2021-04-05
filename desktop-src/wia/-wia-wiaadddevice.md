---
description: La funzione WiaAddDevice richiama l'interfaccia utente dell'installazione guidata dello scanner e della fotocamera. Equivale a eseguire &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; dal prompt dei comandi.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Funzione WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751751"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="bd504-104">WiaAddDevice (funzione)</span><span class="sxs-lookup"><span data-stu-id="bd504-104">WiaAddDevice function</span></span>

<span data-ttu-id="bd504-105">La funzione **WiaAddDevice** richiama l'interfaccia utente dell'installazione guidata dello scanner e della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="bd504-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="bd504-106">È equivalente all'esecuzione di "rundll32.exe STI \_ci.dll AddDevice" dal prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="bd504-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd504-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd504-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="bd504-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd504-108">Parameters</span></span>

<span data-ttu-id="bd504-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="bd504-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd504-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd504-110">Return value</span></span>

<span data-ttu-id="bd504-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bd504-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd504-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd504-112">Remarks</span></span>

<span data-ttu-id="bd504-113">Questa funzione deve essere chiamata con le credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="bd504-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="bd504-114">Quando si esegue il controllo dell'account utente (LUA), il processo deve essere elevato.</span><span class="sxs-lookup"><span data-stu-id="bd504-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd504-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd504-115">Requirements</span></span>



| <span data-ttu-id="bd504-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd504-116">Requirement</span></span> | <span data-ttu-id="bd504-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bd504-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd504-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd504-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd504-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd504-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd504-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd504-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd504-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd504-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bd504-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd504-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd504-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd504-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="bd504-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd504-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd504-125"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd504-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd504-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd504-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd504-127">**InstallWiaDevice**</span><span class="sxs-lookup"><span data-stu-id="bd504-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




