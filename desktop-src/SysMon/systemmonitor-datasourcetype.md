---
title: Proprietà DataSourceType di SystemMonitor
description: Recupera o imposta l'origine dei dati del contatore delle prestazioni.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Proprietà DataSourceType SysMon
- Proprietà DataSourceType SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048579"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="cf393-106">SystemMonitor::D Proprietà ataSourceType</span><span class="sxs-lookup"><span data-stu-id="cf393-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="cf393-107">Recupera o imposta l'origine dei dati del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cf393-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf393-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf393-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="cf393-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cf393-109">Property value</span></span>

<span data-ttu-id="cf393-110">Origine dei dati del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cf393-110">Source of the performance counter data.</span></span> <span data-ttu-id="cf393-111">Per i valori possibili, vedere [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="cf393-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="cf393-112">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="cf393-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf393-113">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="cf393-113">Exception type</span></span></th>
<th><span data-ttu-id="cf393-114">Condizione</span><span class="sxs-lookup"><span data-stu-id="cf393-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf393-115"><strong>System. ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="cf393-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="cf393-116">È possibile ricevere questa eccezione per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf393-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="cf393-117">Il valore dell'origine dati specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="cf393-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="cf393-118">Se l'origine dati è un file di log, SYSMON non è in grado di trovare uno dei file specificati.</span><span class="sxs-lookup"><span data-stu-id="cf393-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="cf393-119">Il valore ERR. Number è 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="cf393-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cf393-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf393-120">Remarks</span></span>

<span data-ttu-id="cf393-121">**Prima di Windows Vista:** Se il valore di questa proprietà è impostato su sysmonLogFiles, non è possibile aggiungere o rimuovere i file di log dalla [**raccolta dei file di log**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="cf393-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="cf393-122">Impostare il valore di questa proprietà su sysmonLogFiles solo dopo la creazione o la modifica della raccolta di file di log.</span><span class="sxs-lookup"><span data-stu-id="cf393-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="cf393-123">Inoltre, non è possibile modificare le proprietà [**SqlDsnName**](systemmonitor-sqldsnname.md) e [**SqlLogSetName**](systemmonitor-sqllogsetname.md) se il valore di questa proprietà non deve essere impostato su sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="cf393-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="cf393-124">Impostare il valore di questa proprietà su sysmonSqlLog solo dopo aver modificato i nomi del server e del database.</span><span class="sxs-lookup"><span data-stu-id="cf393-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf393-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf393-125">Requirements</span></span>



| <span data-ttu-id="cf393-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf393-126">Requirement</span></span> | <span data-ttu-id="cf393-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cf393-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf393-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf393-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf393-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf393-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cf393-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf393-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf393-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf393-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf393-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cf393-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf393-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cf393-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf393-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf393-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf393-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="cf393-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





