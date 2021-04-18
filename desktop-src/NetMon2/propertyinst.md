---
description: La struttura PROPERTYINST definisce un'istanza di una proprietà in un elemento di dati riconosciuti. Network Monitor alloca e compila una struttura PROPERTYINST quando una proprietà è associata all'acquisizione.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Struttura PROPERTYINST (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310961"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="1c71d-104">Struttura PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="1c71d-104">PROPERTYINST structure</span></span>

<span data-ttu-id="1c71d-105">La struttura **PROPERTYINST** definisce un'istanza di una proprietà in un elemento di dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="1c71d-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="1c71d-106">Network Monitor alloca e compila una struttura **PROPERTYINST** quando una proprietà è associata all'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1c71d-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c71d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c71d-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="1c71d-108">Members</span><span class="sxs-lookup"><span data-stu-id="1c71d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1c71d-109">**lpPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1c71d-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-110">Puntatore alla struttura [PROPERTYINFO](propertyinfo.md) che definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c71d-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-111">**szPropertyText**</span><span class="sxs-lookup"><span data-stu-id="1c71d-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-112">Puntatore a una stringa visualizzata nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="1c71d-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-113">**lpData**</span><span class="sxs-lookup"><span data-stu-id="1c71d-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-114">Puntatore all'inizio dei dati per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c71d-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="1c71d-115">Il parser determina la posizione in cui vengono avviati i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c71d-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="1c71d-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-117">Puntatore ai dati **byte** .</span><span class="sxs-lookup"><span data-stu-id="1c71d-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-118">**lpWord**</span><span class="sxs-lookup"><span data-stu-id="1c71d-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-119">Puntatore ai dati di **Word** .</span><span class="sxs-lookup"><span data-stu-id="1c71d-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-120">**lpDword**</span><span class="sxs-lookup"><span data-stu-id="1c71d-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-121">Puntatore ai dati **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1c71d-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-122">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="1c71d-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-123">Puntatore ai dati [**largeInt**](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="1c71d-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-124">**lpSysTime**</span><span class="sxs-lookup"><span data-stu-id="1c71d-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-125">Puntatore ai dati di [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="1c71d-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-126">**lpPropertyInstEx**</span><span class="sxs-lookup"><span data-stu-id="1c71d-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-127">Puntatore a una struttura [PROPERTYINSTEX](propertyinstex.md) .</span><span class="sxs-lookup"><span data-stu-id="1c71d-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="1c71d-128">Il membro **lpPropertyInstEx** viene usato solo quando si chiama [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span><span class="sxs-lookup"><span data-stu-id="1c71d-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="1c71d-129">Se si usa **lpPropertyInstEx** , è necessario impostare il membro **DataLength** su 0xffff.</span><span class="sxs-lookup"><span data-stu-id="1c71d-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="1c71d-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-131">Lunghezza dei dati per questa istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c71d-131">Data length for this instance of the property.</span></span> <span data-ttu-id="1c71d-132">Se il membro **lpPropertyInstEx** punta a una struttura [**PROPERTYINSTEX**](propertyinstex.md) , è necessario impostare **DataLength** su 0xffff.</span><span class="sxs-lookup"><span data-stu-id="1c71d-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-133">**Level**</span><span class="sxs-lookup"><span data-stu-id="1c71d-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-134">Informazioni sul livello.</span><span class="sxs-lookup"><span data-stu-id="1c71d-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="1c71d-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-136">Identificatore del contesto del file della guida.</span><span class="sxs-lookup"><span data-stu-id="1c71d-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1c71d-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="1c71d-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1c71d-138">Flag di condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1c71d-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c71d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c71d-139">Remarks</span></span>

<span data-ttu-id="1c71d-140">La struttura **PROPERTYINST** definisce un'istanza di una proprietà associata.</span><span class="sxs-lookup"><span data-stu-id="1c71d-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="1c71d-141">Il parser accede alla struttura **PROPERTYINST** tramite varie funzioni helper.</span><span class="sxs-lookup"><span data-stu-id="1c71d-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="1c71d-142">Ad esempio, quando viene chiamata la funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per formattare i dati di una proprietà, viene modificato il membro **SzPropertyText** della struttura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="1c71d-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c71d-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c71d-143">Requirements</span></span>



| <span data-ttu-id="1c71d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c71d-144">Requirement</span></span> | <span data-ttu-id="1c71d-145">Valore</span><span class="sxs-lookup"><span data-stu-id="1c71d-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c71d-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c71d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1c71d-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1c71d-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1c71d-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c71d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1c71d-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1c71d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1c71d-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c71d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c71d-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c71d-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c71d-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c71d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c71d-153">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="1c71d-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="1c71d-154">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="1c71d-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

