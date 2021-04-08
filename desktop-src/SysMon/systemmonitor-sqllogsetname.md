---
title: Proprietà SqlLogSetName di SystemMonitor
description: Recupera o imposta il nome descrittivo del set di log.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Proprietà SqlLogSetName SysMon
- Proprietà SqlLogSetName SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047819"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="2ecc0-106">Proprietà SystemMonitor:: SqlLogSetName</span><span class="sxs-lookup"><span data-stu-id="2ecc0-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="2ecc0-107">Recupera o imposta il nome descrittivo del set di log.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecc0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ecc0-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="2ecc0-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2ecc0-109">Property value</span></span>

<span data-ttu-id="2ecc0-110">Nome descrittivo del set di log, che corrisponde a un singolo file di log contenente dati binari o di testo nel database SQL.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecc0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ecc0-111">Remarks</span></span>

<span data-ttu-id="2ecc0-112">**Prima di Windows Vista:** Non è possibile modificare questa proprietà se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="2ecc0-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecc0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ecc0-113">Requirements</span></span>



| <span data-ttu-id="2ecc0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ecc0-114">Requirement</span></span> | <span data-ttu-id="2ecc0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2ecc0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecc0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ecc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecc0-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ecc0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2ecc0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ecc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecc0-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ecc0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ecc0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2ecc0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ecc0-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc0-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecc0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ecc0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecc0-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="2ecc0-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="2ecc0-124">**SystemMonitor. SqlDsnName**</span><span class="sxs-lookup"><span data-stu-id="2ecc0-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





