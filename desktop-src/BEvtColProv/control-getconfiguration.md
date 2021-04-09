---
description: Leggere la configurazione attiva dell'agente di raccolta.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Metodo GetConfiguration della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965912"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="511fa-103">Metodo GetConfiguration della classe Control</span><span class="sxs-lookup"><span data-stu-id="511fa-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="511fa-104">Leggere la configurazione attiva dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="511fa-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="511fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="511fa-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="511fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="511fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511fa-107">*TimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="511fa-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="511fa-108">Quando questo metodo restituisce un risultato, questo parametro contiene i bit di ordine inferiore di un timestamp che indica quando è stata impostata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="511fa-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="511fa-109">*TimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="511fa-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="511fa-110">Quando questo metodo viene restituito, questo parametro contiene i bit più significativi di un timestamp che indica quando è stata impostata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="511fa-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511fa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="511fa-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="511fa-112">0</span><span class="sxs-lookup"><span data-stu-id="511fa-112">0</span></span>

<span data-ttu-id="511fa-113">Errore</span><span class="sxs-lookup"><span data-stu-id="511fa-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="511fa-114">1</span><span class="sxs-lookup"><span data-stu-id="511fa-114">1</span></span>

<span data-ttu-id="511fa-115">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="511fa-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="511fa-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="511fa-116">Requirements</span></span>



| <span data-ttu-id="511fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="511fa-117">Requirement</span></span> | <span data-ttu-id="511fa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="511fa-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="511fa-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="511fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="511fa-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="511fa-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="511fa-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="511fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="511fa-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="511fa-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="511fa-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="511fa-123">Namespace</span></span><br/>                | <span data-ttu-id="511fa-124">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="511fa-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="511fa-125">MOF</span><span class="sxs-lookup"><span data-stu-id="511fa-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="511fa-126"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="511fa-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="511fa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="511fa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="511fa-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="511fa-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="511fa-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="511fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511fa-130">**Control**</span><span class="sxs-lookup"><span data-stu-id="511fa-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




