---
description: Restituisce l'elenco dei file di configurazione del backup salvati che è possibile ripristinare.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Metodo ListBackups della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125838"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="9490e-103">Metodo ListBackups della classe Control</span><span class="sxs-lookup"><span data-stu-id="9490e-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="9490e-104">Restituisce l'elenco dei file di configurazione del backup salvati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="9490e-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="9490e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9490e-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="9490e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9490e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9490e-107">*OriginalTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9490e-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9490e-108">Timestamp di quando è stata impostata la configurazione corrente, se ripristinata dal backup, conterrà il timestamp originale.</span><span class="sxs-lookup"><span data-stu-id="9490e-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="9490e-109">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9490e-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9490e-110">*OriginalTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9490e-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9490e-111">Timestamp di quando è stata impostata la configurazione corrente, se ripristinata dal backup, conterrà il timestamp originale.</span><span class="sxs-lookup"><span data-stu-id="9490e-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="9490e-112">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9490e-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9490e-113">*File* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9490e-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9490e-114">Elenco di file di backup disponibili, in ordine dal più recente al meno recente.</span><span class="sxs-lookup"><span data-stu-id="9490e-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="9490e-115">*FilesTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9490e-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9490e-116">Per ogni file di backup, il timestamp di quando è stata impostata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="9490e-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="9490e-117">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9490e-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9490e-118">*FilesTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9490e-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9490e-119">Per ogni file di backup, il timestamp di quando è stata impostata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="9490e-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="9490e-120">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9490e-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9490e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9490e-121">Return value</span></span>

<span data-ttu-id="9490e-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9490e-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9490e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9490e-123">Requirements</span></span>



| <span data-ttu-id="9490e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9490e-124">Requirement</span></span> | <span data-ttu-id="9490e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9490e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9490e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9490e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9490e-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9490e-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9490e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9490e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9490e-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9490e-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="9490e-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9490e-130">Namespace</span></span><br/>                | <span data-ttu-id="9490e-131">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="9490e-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="9490e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9490e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9490e-133"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9490e-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="9490e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9490e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9490e-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9490e-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9490e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9490e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9490e-137">**Control**</span><span class="sxs-lookup"><span data-stu-id="9490e-137">**Control**</span></span>](control.md)
</dt> </dl>

 

