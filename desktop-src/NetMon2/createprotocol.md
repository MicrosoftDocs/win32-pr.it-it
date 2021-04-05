---
description: La funzione CreateProtocol notifica Network Monitor che esiste un parser di protocollo specifico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Funzione CreateProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131858"
---
# <a name="createprotocol-function"></a><span data-ttu-id="b68b9-103">CreateProtocol (funzione)</span><span class="sxs-lookup"><span data-stu-id="b68b9-103">CreateProtocol function</span></span>

<span data-ttu-id="b68b9-104">La funzione **CreateProtocol** notifica Network Monitor che esiste un parser di protocollo specifico.</span><span class="sxs-lookup"><span data-stu-id="b68b9-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="b68b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b68b9-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="b68b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b68b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b68b9-107">*ProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b68b9-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68b9-108">Nome del protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="b68b9-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="b68b9-109">*lpEntryPoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b68b9-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68b9-110">Struttura [ENTRYPOINTS](entrypoints.md) che contiene i punti di ingresso rimanenti della dll del parser.</span><span class="sxs-lookup"><span data-stu-id="b68b9-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="b68b9-111">Vedere la sezione Osservazioni per un elenco delle funzioni di esportazione a cui fa riferimento ogni punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="b68b9-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="b68b9-112">I punti di ingresso devono essere specificati nell'ordine specificato dalla struttura **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="b68b9-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="b68b9-113">*cbEntryPoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b68b9-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b68b9-114">Dimensione della struttura **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="b68b9-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="b68b9-115">Network Monitor fornisce una \_ macro di dimensioni ENTRYPOINTS che è possibile usare per specificare le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="b68b9-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b68b9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b68b9-116">Return value</span></span>

<span data-ttu-id="b68b9-117">Se la funzione ha esito positivo, il valore restituito è un handle per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="b68b9-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="b68b9-118">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="b68b9-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b68b9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b68b9-119">Remarks</span></span>

<span data-ttu-id="b68b9-120">La DLL del parser chiama **CreateProtocol** durante la relativa implementazione di [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="b68b9-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="b68b9-121">La funzione **CreateProtocol** viene chiamata quando il sistema operativo carica la dll del parser per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="b68b9-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="b68b9-122">I punti di ingresso a cui viene fatto riferimento nel parametro *lpEntryPoints* includono i puntatori alle funzioni di esportazione seguenti che devono essere fornite nell'ordine presentato qui.</span><span class="sxs-lookup"><span data-stu-id="b68b9-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="b68b9-123">Registra</span><span class="sxs-lookup"><span data-stu-id="b68b9-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="b68b9-124">Annullamento registrazione</span><span class="sxs-lookup"><span data-stu-id="b68b9-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="b68b9-125">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="b68b9-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="b68b9-126">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="b68b9-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="b68b9-127">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="b68b9-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="b68b9-128">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="b68b9-128">For information on</span></span>                                                                                 | <span data-ttu-id="b68b9-129">Vedere</span><span class="sxs-lookup"><span data-stu-id="b68b9-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b68b9-130">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="b68b9-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="b68b9-131">Parser</span><span class="sxs-lookup"><span data-stu-id="b68b9-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="b68b9-132">Come implementare **DllMain** include un esempio di chiamata a **CreateProtocol** all'interno di **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="b68b9-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="b68b9-133">Implementazione di DllMain</span><span class="sxs-lookup"><span data-stu-id="b68b9-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="b68b9-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b68b9-134">Requirements</span></span>



| <span data-ttu-id="b68b9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b68b9-135">Requirement</span></span> | <span data-ttu-id="b68b9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b9-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b68b9-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b68b9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b68b9-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b68b9-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b68b9-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b68b9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b68b9-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b68b9-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b68b9-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b68b9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b68b9-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b68b9-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b68b9-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="b68b9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b68b9-144"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b68b9-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b68b9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b68b9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b68b9-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b68b9-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b68b9-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b68b9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68b9-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="b68b9-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

