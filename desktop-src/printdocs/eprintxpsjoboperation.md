---
description: Specifica se un processo di stampa XPS si trova nella fase di spooling o di rendering.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumerazione EPrintXPSJobOperation (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756392"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="75896-103">Enumerazione EPrintXPSJobOperation</span><span class="sxs-lookup"><span data-stu-id="75896-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="75896-104">Specifica se un processo di stampa XPS si trova nella fase di spooling o di rendering.</span><span class="sxs-lookup"><span data-stu-id="75896-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="75896-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75896-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="75896-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="75896-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="75896-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span><span class="sxs-lookup"><span data-stu-id="75896-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="75896-108">Il processo XPS sta effettuando lo spooling.</span><span class="sxs-lookup"><span data-stu-id="75896-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="75896-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span><span class="sxs-lookup"><span data-stu-id="75896-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="75896-110">Viene eseguito il rendering del processo XPS.</span><span class="sxs-lookup"><span data-stu-id="75896-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75896-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="75896-111">Remarks</span></span>

<span data-ttu-id="75896-112">Questa enumerazione viene utilizzata principalmente come parametro per la funzione [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="75896-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75896-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75896-113">Requirements</span></span>



| <span data-ttu-id="75896-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75896-114">Requirement</span></span> | <span data-ttu-id="75896-115">Valore</span><span class="sxs-lookup"><span data-stu-id="75896-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75896-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75896-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75896-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75896-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="75896-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75896-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75896-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75896-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75896-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75896-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75896-121"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75896-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




