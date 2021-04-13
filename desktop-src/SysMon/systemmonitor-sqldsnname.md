---
title: Proprietà SqlDsnName di SystemMonitor
description: Recupera o imposta il nome dell'origine dati (DSN) ODBC.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Proprietà SqlDsnName SysMon
- Proprietà SqlDsnName SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400208"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="bd922-106">Proprietà SystemMonitor:: SqlDsnName</span><span class="sxs-lookup"><span data-stu-id="bd922-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="bd922-107">Recupera o imposta il nome dell'origine dati (DSN) ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd922-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd922-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd922-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="bd922-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bd922-109">Property value</span></span>

<span data-ttu-id="bd922-110">Nome dell'origine dati ODBC che punta a un database contenente le tabelle PerfMon corrette.</span><span class="sxs-lookup"><span data-stu-id="bd922-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="bd922-111">Il formato è SQL: DSN.</span><span class="sxs-lookup"><span data-stu-id="bd922-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd922-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd922-112">Remarks</span></span>

<span data-ttu-id="bd922-113">Per generare il file di log SQL, è necessario utilizzare lo snap-in MMC Perfmon. msc.</span><span class="sxs-lookup"><span data-stu-id="bd922-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="bd922-114">I registri dei contatori si trovano in **avvisi e registri di prestazioni**.</span><span class="sxs-lookup"><span data-stu-id="bd922-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="bd922-115">Per specificare un log SQL, fare clic con il pulsante destro del mouse sul file di log creato e scegliere **Proprietà** dal menu.</span><span class="sxs-lookup"><span data-stu-id="bd922-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="bd922-116">Nella pagina delle proprietà **file di registro** selezionare **database SQL** dall'elenco a discesa **tipo file di log** .</span><span class="sxs-lookup"><span data-stu-id="bd922-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="bd922-117">**Prima di Windows Vista:** Non è possibile modificare questa proprietà se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="bd922-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="bd922-118">È necessario innanzitutto specificare il nome e quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonSqlLog**.</span><span class="sxs-lookup"><span data-stu-id="bd922-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd922-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd922-119">Requirements</span></span>



| <span data-ttu-id="bd922-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd922-120">Requirement</span></span> | <span data-ttu-id="bd922-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bd922-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd922-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd922-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd922-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd922-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bd922-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd922-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd922-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd922-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd922-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bd922-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd922-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bd922-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd922-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd922-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd922-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="bd922-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bd922-130">**SystemMonitor. SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="bd922-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





