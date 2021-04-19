---
description: La funzione AttachPropertyInstanceEx esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Funzione AttachPropertyInstanceEx (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311643"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="931d6-103">AttachPropertyInstanceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="931d6-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="931d6-104">La funzione **AttachPropertyInstanceEx** esegue il mapping di una proprietà esistente a una posizione specifica nei dati riconosciuti e modifica il valore dei dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="931d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="931d6-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="931d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="931d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="931d6-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-108">Handle per il frame da analizzare.</span><span class="sxs-lookup"><span data-stu-id="931d6-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="931d6-109">Usare l'handle passato alla DLL del parser nel parametro *hFrame* della funzione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="931d6-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-110">*hProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-111">Handle per una struttura [**PROPERTYINFO**](propertyinfo.md) che definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="931d6-112">Quando si implementa la funzione di esportazione del [**Registro**](register-parser.md) , è necessario specificare la struttura **PROPERTYINFO** che definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-113">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-114">Lunghezza dei dati per questa istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-115">*lpData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-116">Puntatore alla posizione nei dati riconosciuti in cui si trova il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="931d6-117">Usare il puntatore passato alla DLL del parser nel parametro *lpProtocol* della funzione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="931d6-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-118">*LengthEx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-119">Lunghezza in byte dei dati estesi.</span><span class="sxs-lookup"><span data-stu-id="931d6-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-120">*lpDataEx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-121">Puntatore ai dati estesi, che è in genere una variabile dello stack che contiene i dati di estensione.</span><span class="sxs-lookup"><span data-stu-id="931d6-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-122">*HelpID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-123">Identificatore (compreso tra 0 e 2047) usato per impostare la Guida sensibile al contesto per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="931d6-124">Il numero *HelpID* è relativo al file della Guida associato al database delle [*Proprietà*](p.md)del protocollo.</span><span class="sxs-lookup"><span data-stu-id="931d6-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="931d6-125">*IndentLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-126">Livello di rientro (compreso tra 0 e 15) utilizzato per visualizzare una proprietà gerarchicamente.</span><span class="sxs-lookup"><span data-stu-id="931d6-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="931d6-127">Network Monitor utilizza i livelli da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="931d6-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="931d6-128">Il livello 15 è un valore speciale che consente al parser di alleghi una proprietà nascosta che non è visibile.</span><span class="sxs-lookup"><span data-stu-id="931d6-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="931d6-129">*IFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="931d6-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931d6-130">Valore del campo di BIT che indica l'ordine dei bit all'interno di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="931d6-131">I parser precedenti che impostano il *ferror* su 0 o 1 devono ora impostare il *ferror* su IFLAG \_ Error.</span><span class="sxs-lookup"><span data-stu-id="931d6-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="931d6-132">Impostare questo parametro su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="931d6-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="931d6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="931d6-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="931d6-134">Significato</span><span class="sxs-lookup"><span data-stu-id="931d6-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="931d6-135"><dt>**\_errore IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="931d6-136">Si è verificato un errore nei dati del frame.</span><span class="sxs-lookup"><span data-stu-id="931d6-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="931d6-137"><dt>**IFLAG \_ scambiati**</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="931d6-138">Al momento della connessione, **Word** byte è un formato non Intel.</span><span class="sxs-lookup"><span data-stu-id="931d6-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="931d6-139"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="931d6-140">Al momento della connessione, la **stringa** è Unicode.</span><span class="sxs-lookup"><span data-stu-id="931d6-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="931d6-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="931d6-141">Return value</span></span>

<span data-ttu-id="931d6-142">Se la funzione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="931d6-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="931d6-143">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="931d6-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="931d6-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="931d6-144">Remarks</span></span>

<span data-ttu-id="931d6-145">La funzione **AttachPropertyInstanceEx** viene chiamata durante l'implementazione della funzione di esportazione [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="931d6-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="931d6-146">Quando una proprietà viene associata ai dati tramite AttachPropertyInstanceEx, Network Monitor crea una struttura [**PROPERTYINST**](propertyinst.md) che definisce l'istanza della proprietà associata e una struttura [**PROPERTYINSTEX**](propertyinstex.md) che definisce i dati estesi.</span><span class="sxs-lookup"><span data-stu-id="931d6-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="931d6-147">Se viene chiamato **AttachPropertyInstanceEx** e non vengono forniti dati estesi, il parametro *lpDataEx* è **null** o il parametro *LengthEx* è 0, la chiamata **AttachPropertyInstanceEx** è equivalente dal punto di vista funzionale a una chiamata [**AttachPropertyInstance**](attachpropertyinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="931d6-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="931d6-148">Durante l'implementazione di [**AttachProperties**](attachproperties.md), chiamare [**AttachPropertyInstance**](attachpropertyinstance.md) per usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="931d6-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="931d6-149">È anche possibile chiamare la funzione **AttachPropertyInstanceEx** per modificare i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="931d6-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="931d6-150">Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="931d6-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="931d6-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="931d6-151">Requirements</span></span>



| <span data-ttu-id="931d6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="931d6-152">Requirement</span></span> | <span data-ttu-id="931d6-153">Valore</span><span class="sxs-lookup"><span data-stu-id="931d6-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="931d6-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="931d6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="931d6-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="931d6-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="931d6-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="931d6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="931d6-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="931d6-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="931d6-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="931d6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="931d6-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="931d6-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="931d6-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="931d6-161"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="931d6-162">DLL</span><span class="sxs-lookup"><span data-stu-id="931d6-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="931d6-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="931d6-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




