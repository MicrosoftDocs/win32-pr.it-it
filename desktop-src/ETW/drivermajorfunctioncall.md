---
description: Questa classe è la classe del tipo di evento per gli eventi di chiamata di funzione principali del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Classe DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977143"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="731cd-104">Classe DriverMajorFunctionCall</span><span class="sxs-lookup"><span data-stu-id="731cd-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="731cd-105">Questa classe è la classe del tipo di evento per gli eventi di chiamata di funzione principali del driver.</span><span class="sxs-lookup"><span data-stu-id="731cd-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="731cd-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="731cd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="731cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="731cd-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="731cd-108">Members</span><span class="sxs-lookup"><span data-stu-id="731cd-108">Members</span></span>

<span data-ttu-id="731cd-109">La classe **DriverMajorFunctionCall** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="731cd-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="731cd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="731cd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="731cd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="731cd-111">Properties</span></span>

<span data-ttu-id="731cd-112">La classe **DriverMajorFunctionCall** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="731cd-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="731cd-113">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="731cd-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-116">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="731cd-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="731cd-117">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di i/O.</span><span class="sxs-lookup"><span data-stu-id="731cd-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="731cd-118">**IRP**</span><span class="sxs-lookup"><span data-stu-id="731cd-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-121">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="731cd-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="731cd-122">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="731cd-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="731cd-123">**MajorFunction**</span><span class="sxs-lookup"><span data-stu-id="731cd-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-126">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="731cd-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="731cd-127">Codice che identifica la funzione principale chiamata.</span><span class="sxs-lookup"><span data-stu-id="731cd-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="731cd-128">**MinorFunction**</span><span class="sxs-lookup"><span data-stu-id="731cd-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-131">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="731cd-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="731cd-132">Codice che idenitifies la funzione secondaria chiamata.</span><span class="sxs-lookup"><span data-stu-id="731cd-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="731cd-133">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="731cd-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-136">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="731cd-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="731cd-137">Indirizzo della funzione di driver chiamata.</span><span class="sxs-lookup"><span data-stu-id="731cd-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="731cd-138">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="731cd-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="731cd-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="731cd-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="731cd-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="731cd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="731cd-141">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="731cd-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="731cd-142">Identificatore che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="731cd-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="731cd-143">Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="731cd-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="731cd-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="731cd-144">Requirements</span></span>



| <span data-ttu-id="731cd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="731cd-145">Requirement</span></span> | <span data-ttu-id="731cd-146">Valore</span><span class="sxs-lookup"><span data-stu-id="731cd-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="731cd-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="731cd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="731cd-148">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="731cd-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="731cd-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="731cd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="731cd-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="731cd-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="731cd-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="731cd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731cd-152">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="731cd-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




