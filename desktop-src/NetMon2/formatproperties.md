---
description: La funzione di esportazione FormatProperties formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. Se si desidera visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione FormatProperties in tutte le dll del parser.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Funzione di callback FormatProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305929"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="d7cbc-104">Funzione di callback FormatProperties</span><span class="sxs-lookup"><span data-stu-id="d7cbc-104">FormatProperties callback function</span></span>

<span data-ttu-id="d7cbc-105">La funzione di esportazione **FormatProperties** formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="d7cbc-106">Se si desidera visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione **FormatProperties** in tutte le dll del parser.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7cbc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7cbc-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="d7cbc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7cbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7cbc-109">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbc-110">Handle per il frame da analizzare.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="d7cbc-111">*lpFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbc-112">Puntatore al primo byte di un frame.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7cbc-113">*lpProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbc-114">Puntatore all'inizio dei dati del protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7cbc-115">*nPropertyInsts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbc-116">Numero di strutture [PROPERTYINST](propertyinst.md) fornite da *lpPropInst*.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="d7cbc-117">*lpPropInst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbc-118">Puntatore a una matrice di strutture [PROPERTYINST](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="d7cbc-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7cbc-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7cbc-119">Return value</span></span>

<span data-ttu-id="d7cbc-120">Se la funzione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="d7cbc-121">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cbc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7cbc-122">Remarks</span></span>

<span data-ttu-id="d7cbc-123">Network Monitor chiama la funzione **FormatProperties** per visualizzare i dati nel riquadro dei dettagli dell'interfaccia utente Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="d7cbc-124">In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="d7cbc-125">Tuttavia, Network Monitor non garantisce il numero di volte che chiama **FormatProperties** per un parser specifico.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="d7cbc-126">Durante l'implementazione della funzione **FormatProperties** , il parser chiama indirettamente la funzione [FormatPropertyInstance](formatpropertyinstance.md) per usare il formattatore generico fornito da Network Monitor oppure può chiamare una routine di formattatore personalizzata definita dal parser.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="d7cbc-127">È necessario chiamare uno dei formattatori per ogni struttura [PROPERTYINST](propertyinst.md) passata alla DLL del parser nel parametro *lpPropInst* .</span><span class="sxs-lookup"><span data-stu-id="d7cbc-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="d7cbc-128">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="d7cbc-128">For Information on</span></span>                                          | <span data-ttu-id="d7cbc-129">Vedere</span><span class="sxs-lookup"><span data-stu-id="d7cbc-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d7cbc-130">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="d7cbc-131">Parser</span><span class="sxs-lookup"><span data-stu-id="d7cbc-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="d7cbc-132">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="d7cbc-133">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="d7cbc-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="d7cbc-134">L'implementazione di **FormatProperties**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="d7cbc-135">Implementazione di FormatProperties</span><span class="sxs-lookup"><span data-stu-id="d7cbc-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="d7cbc-136">In che modo il formattatore generico formatta tipi diversi di dati.</span><span class="sxs-lookup"><span data-stu-id="d7cbc-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="d7cbc-137">Output formattatore generico</span><span class="sxs-lookup"><span data-stu-id="d7cbc-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="d7cbc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7cbc-138">Requirements</span></span>



| <span data-ttu-id="d7cbc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7cbc-139">Requirement</span></span> | <span data-ttu-id="d7cbc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="d7cbc-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7cbc-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7cbc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d7cbc-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7cbc-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7cbc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d7cbc-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7cbc-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7cbc-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7cbc-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7cbc-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7cbc-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7cbc-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7cbc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7cbc-148">FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="d7cbc-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="d7cbc-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="d7cbc-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="d7cbc-150">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="d7cbc-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




