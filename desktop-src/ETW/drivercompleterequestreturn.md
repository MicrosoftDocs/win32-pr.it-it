---
description: Questa classe è la classe del tipo di evento per gli eventi di restituzione di richieste complete del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Classe DriverCompleteRequestReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525255"
---
# <a name="drivercompleterequestreturn-class"></a><span data-ttu-id="dec76-104">Classe DriverCompleteRequestReturn</span><span class="sxs-lookup"><span data-stu-id="dec76-104">DriverCompleteRequestReturn class</span></span>

<span data-ttu-id="dec76-105">Questa classe è la classe del tipo di evento per gli eventi di restituzione di richieste complete del driver.</span><span class="sxs-lookup"><span data-stu-id="dec76-105">This class is the event type class for driver complete request return events.</span></span>

<span data-ttu-id="dec76-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="dec76-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec76-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dec76-107">Syntax</span></span>

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="dec76-108">Members</span><span class="sxs-lookup"><span data-stu-id="dec76-108">Members</span></span>

<span data-ttu-id="dec76-109">La classe **DriverCompleteRequestReturn** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dec76-109">The **DriverCompleteRequestReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="dec76-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dec76-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dec76-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dec76-111">Properties</span></span>

<span data-ttu-id="dec76-112">La classe **DriverCompleteRequestReturn** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dec76-112">The **DriverCompleteRequestReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dec76-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="dec76-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec76-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dec76-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dec76-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dec76-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec76-116">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="dec76-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dec76-117">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="dec76-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="dec76-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="dec76-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec76-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dec76-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dec76-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dec76-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec76-121">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="dec76-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="dec76-122">Identificatore che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dec76-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="dec76-123">Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="dec76-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dec76-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dec76-124">Requirements</span></span>



| <span data-ttu-id="dec76-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec76-125">Requirement</span></span> | <span data-ttu-id="dec76-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dec76-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dec76-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec76-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dec76-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dec76-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dec76-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec76-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dec76-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dec76-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dec76-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dec76-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec76-132">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="dec76-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




