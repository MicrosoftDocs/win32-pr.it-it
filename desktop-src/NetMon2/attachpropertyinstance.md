---
description: La funzione AttachPropertyInstance esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Funzione AttachPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883674"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="15695-103">AttachPropertyInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="15695-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="15695-104">La funzione **AttachPropertyInstance** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="15695-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15695-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15695-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="15695-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15695-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-108">Handle per il frame da analizzare.</span><span class="sxs-lookup"><span data-stu-id="15695-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="15695-109">Usare l'handle passato alla DLL del parser nel parametro *hFrame* della funzione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="15695-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="15695-110">*hProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-111">Handle per una struttura [**PROPERTYINFO**](propertyinfo.md) che definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="15695-112">Quando si implementa la funzione di esportazione del [**Registro**](register-parser.md) , è necessario specificare la struttura **PROPERTYINFO** che definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="15695-113">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-114">Lunghezza dei dati per questa istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="15695-115">*lpData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-116">Puntatore alla posizione nei dati riconosciuti in cui si trova il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="15695-117">Usare il puntatore passato alla DLL del parser nel parametro *lpProtocol* della funzione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="15695-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="15695-118">*HelpID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-119">Identificatore (compreso tra 0 e 2047) usato per impostare la Guida sensibile al contesto per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="15695-120">Il numero dell'identificatore è relativo al file della Guida associato al [*database della proprietà*](p.md)del protocollo.</span><span class="sxs-lookup"><span data-stu-id="15695-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="15695-121">*IndentLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-122">Livello di rientro (compreso tra 0 e 15) utilizzato per visualizzare una proprietà gerarchicamente.</span><span class="sxs-lookup"><span data-stu-id="15695-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="15695-123">Network Monitor utilizza i livelli da 0 a 14 per rientrare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="15695-124">Il livello 15 è un valore speciale che consente a un parser di alleghi una proprietà nascosta che non è visibile.</span><span class="sxs-lookup"><span data-stu-id="15695-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="15695-125">*IFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-126">Valore del campo di BIT che indica l'ordine dei bit all'interno di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="15695-127">I parser precedenti che impostano il *ferror* su 0 o 1 devono ora impostare il *ferror* su IFLAG \_ Error.</span><span class="sxs-lookup"><span data-stu-id="15695-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="15695-128">Impostare questo parametro su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="15695-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="15695-129">Valore</span><span class="sxs-lookup"><span data-stu-id="15695-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="15695-130">Significato</span><span class="sxs-lookup"><span data-stu-id="15695-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="15695-131"><dt>**\_errore IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="15695-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="15695-132">Si è verificato un errore nei dati del frame.</span><span class="sxs-lookup"><span data-stu-id="15695-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="15695-133"><dt>**IFLAG \_ scambiati**</dt></span><span class="sxs-lookup"><span data-stu-id="15695-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="15695-134">Al momento della connessione, **Word** byte è un formato non Intel.</span><span class="sxs-lookup"><span data-stu-id="15695-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="15695-135"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="15695-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="15695-136">Al momento della connessione, la **stringa** è Unicode.</span><span class="sxs-lookup"><span data-stu-id="15695-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15695-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15695-137">Return value</span></span>

<span data-ttu-id="15695-138">Se la funzione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="15695-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="15695-139">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="15695-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15695-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="15695-140">Remarks</span></span>

<span data-ttu-id="15695-141">La funzione **AttachPropertyInstance** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="15695-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="15695-142">Quando una proprietà è associata ai dati, Network Monitor crea una struttura [**PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata.</span><span class="sxs-lookup"><span data-stu-id="15695-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="15695-143">Durante l'implementazione di [**AttachProperties**](attachproperties.md), chiamare **AttachPropertyInstance** per usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="15695-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="15695-144">È anche possibile chiamare la funzione [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) per modificare i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="15695-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="15695-145">Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="15695-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="15695-146">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="15695-146">For Information on</span></span>                                        | <span data-ttu-id="15695-147">Vedere</span><span class="sxs-lookup"><span data-stu-id="15695-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="15695-148">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="15695-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="15695-149">**Parser**</span><span class="sxs-lookup"><span data-stu-id="15695-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="15695-150">Come chiamare **AttachPropertyInstance**.</span><span class="sxs-lookup"><span data-stu-id="15695-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="15695-151">Implementazione di AttachProperties</span><span class="sxs-lookup"><span data-stu-id="15695-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="15695-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15695-152">Requirements</span></span>



| <span data-ttu-id="15695-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="15695-153">Requirement</span></span> | <span data-ttu-id="15695-154">Valore</span><span class="sxs-lookup"><span data-stu-id="15695-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15695-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15695-155">Minimum supported client</span></span><br/> | <span data-ttu-id="15695-156">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15695-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="15695-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15695-157">Minimum supported server</span></span><br/> | <span data-ttu-id="15695-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15695-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15695-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15695-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="15695-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15695-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="15695-161">Libreria</span><span class="sxs-lookup"><span data-stu-id="15695-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="15695-162"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15695-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="15695-163">DLL</span><span class="sxs-lookup"><span data-stu-id="15695-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15695-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15695-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15695-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15695-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15695-166">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="15695-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="15695-167">**AttachPropertyInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="15695-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="15695-168">**PROPERTYINST**</span><span class="sxs-lookup"><span data-stu-id="15695-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




