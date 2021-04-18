---
description: Formatta i dati dell'istanza della proprietà utilizzando il formattatore generico fornito da Network Monitor.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Funzione FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305928"
---
# <a name="formatpropertyinstance-function"></a><span data-ttu-id="27c1d-103">FormatPropertyInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="27c1d-103">FormatPropertyInstance function</span></span>

<span data-ttu-id="27c1d-104">La funzione **FormatPropertyInstance** formatta i dati dell'istanza della proprietà utilizzando il formattatore generico fornito da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="27c1d-104">The **FormatPropertyInstance** function formats the property instance data using the generic formatter that Network Monitor provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27c1d-105">Syntax</span></span>


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a><span data-ttu-id="27c1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27c1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c1d-107">*lpPropertyInst* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="27c1d-107">*lpPropertyInst* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c1d-108">Puntatore a una struttura [PROPERTYINST](propertyinst.md) che contiene i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="27c1d-108">A pointer to a [PROPERTYINST](propertyinst.md) structure that contains the instance data.</span></span>

<span data-ttu-id="27c1d-109">In input il formattatore generico accetta i dati dell'istanza da uno dei membri di Unione **PROPERTYINST** e li converte in una stringa formattata predefinita.</span><span class="sxs-lookup"><span data-stu-id="27c1d-109">On input, the generic formatter takes the instance data from one of the **PROPERTYINST** union members and converts that data to a predefined formatted string.</span></span>

<span data-ttu-id="27c1d-110">Nell'output il formattatore generico imposta il membro **szPropertyText** della struttura **PROPERTYINST** su un puntatore alla stringa formattata.</span><span class="sxs-lookup"><span data-stu-id="27c1d-110">On output, the generic formatter sets the **szPropertyText** member of the **PROPERTYINST** structure to a pointer to the formatted string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c1d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27c1d-111">Return value</span></span>

<span data-ttu-id="27c1d-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="27c1d-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="27c1d-113">Se la funzione ha esito negativo, il valore restituito è un codice di errore di NMerr. h.</span><span class="sxs-lookup"><span data-stu-id="27c1d-113">If the function is unsuccessful, the return value is an error code from NMerr.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c1d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="27c1d-114">Remarks</span></span>

<span data-ttu-id="27c1d-115">La DLL del parser chiama indirettamente la funzione **FormatPropertyInstance** quando il formattatore generico è necessario per formattare i dati per la visualizzazione nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="27c1d-115">The parser DLL indirectly calls the **FormatPropertyInstance** function when the generic formatter is required to format data for display in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="27c1d-116">Per chiamare **FormatPropertyInstance** , specificarlo nel membro **InstanceData** della struttura [PROPERTYINFO](propertyinfo.md) quando si definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="27c1d-116">To call **FormatPropertyInstance** specify it in the **InstanceData** member of the [PROPERTYINFO](propertyinfo.md) structure when you define the property.</span></span>

> [!Note]  
> <span data-ttu-id="27c1d-117">Il parser non riconosce la funzione chiamata quando deve formattare un'istanza di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="27c1d-117">The parser does not recognize which function is called when it must format an instance of a property.</span></span> <span data-ttu-id="27c1d-118">La funzione può essere **FormatPropertyInstance** o una funzione di formato personalizzata definita dal parser.</span><span class="sxs-lookup"><span data-stu-id="27c1d-118">The function can be **FormatPropertyInstance** or a custom format function defined by the parser.</span></span> <span data-ttu-id="27c1d-119">Il parser chiama qualsiasi funzione format specificata dal membro **InstanceData** della struttura **PROPERTYINFO** per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="27c1d-119">The parser calls whatever format function is specified by the **InstanceData** member of the **PROPERTYINFO** structure for the property.</span></span>

 

<span data-ttu-id="27c1d-120">Per ulteriori informazioni e un esempio di come implementare [formatproperties](formatproperties.md), vedere [implementazione di formatproperties](implementing-formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="27c1d-120">For more information and an example of how to implement [formatproperties](formatproperties.md), see [Implementing FormatProperties](implementing-formatproperties.md).</span></span> <span data-ttu-id="27c1d-121">Per altre informazioni su come il formattatore generico formatta tipi diversi di dati, vedere [output del formattatore generico](generic-formatter-output.md).</span><span class="sxs-lookup"><span data-stu-id="27c1d-121">For more information about how the generic formatter formats different types of data, see [Generic Formatter Output](generic-formatter-output.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c1d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c1d-122">Requirements</span></span>



| <span data-ttu-id="27c1d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c1d-123">Requirement</span></span> | <span data-ttu-id="27c1d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="27c1d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27c1d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c1d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="27c1d-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27c1d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="27c1d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c1d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="27c1d-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27c1d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="27c1d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27c1d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c1d-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c1d-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="27c1d-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="27c1d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="27c1d-132"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27c1d-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="27c1d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="27c1d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c1d-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c1d-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c1d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27c1d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c1d-136">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="27c1d-136">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="27c1d-137">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="27c1d-137">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




