---
description: La funzione di esportazione DllMain per il parser identifica l'esistenza del parser e rilascia le risorse utilizzate da Network Monitor per il parser. DllMain deve essere implementato in tutte le dll del parser.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Funzione di callback del parser DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314176"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="e56e8-104">Funzione di callback del parser DllMain</span><span class="sxs-lookup"><span data-stu-id="e56e8-104">DllMain Parser callback function</span></span>

<span data-ttu-id="e56e8-105">La funzione di esportazione **DllMain** per il parser identifica l'esistenza del parser e rilascia le risorse utilizzate da Network Monitor per il parser.</span><span class="sxs-lookup"><span data-stu-id="e56e8-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="e56e8-106">**DllMain** deve essere implementato in tutte le dll del parser.</span><span class="sxs-lookup"><span data-stu-id="e56e8-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e56e8-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="e56e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e56e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56e8-109">*HINSTANCE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e56e8-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56e8-110">Handle per un'istanza del parser.</span><span class="sxs-lookup"><span data-stu-id="e56e8-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="e56e8-111">*Comando* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e56e8-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56e8-112">Indicatore per determinare il motivo per cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="e56e8-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="e56e8-113">Per un elenco di tutti i flag possibili, vedere [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="e56e8-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="e56e8-114">L'implementazione del parser deve elaborare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e56e8-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="e56e8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e56e8-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="e56e8-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e56e8-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="e56e8-117"><dt>**\_connessione processo \_ dll**</dt></span><span class="sxs-lookup"><span data-stu-id="e56e8-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="e56e8-118">Quando **DllMain** viene chiamato per la prima volta, è necessario che la dll chiami [CreateProtocol](createprotocol.md) per fornire informazioni a Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="e56e8-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="e56e8-119"><dt>**\_ \_ scollegamento processo dll**</dt></span><span class="sxs-lookup"><span data-stu-id="e56e8-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="e56e8-120">Quando **DllMain** viene chiamato per l'ultima volta, è necessario che la dll chiami [DestroyProtocol](destroyprotocol.md) per rilasciare le risorse utilizzate dalla dll.</span><span class="sxs-lookup"><span data-stu-id="e56e8-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e56e8-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="e56e8-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="e56e8-122">Non usato adesso.</span><span class="sxs-lookup"><span data-stu-id="e56e8-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56e8-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e56e8-123">Return value</span></span>

<span data-ttu-id="e56e8-124">La DLL del parser restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="e56e8-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e56e8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e56e8-125">Remarks</span></span>

<span data-ttu-id="e56e8-126">Il sistema operativo chiama **DllMain** per caricare e scaricare la dll del parser.</span><span class="sxs-lookup"><span data-stu-id="e56e8-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="e56e8-127">Questa funzione è basata sulla funzione [DllMain](/windows/desktop/Dlls/dllmain) della libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="e56e8-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="e56e8-128">È inoltre possibile utilizzare l'implementazione di **DllMain** per archiviare un'istanza di un parser da utilizzare in futuro.</span><span class="sxs-lookup"><span data-stu-id="e56e8-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="e56e8-129">Ad esempio, è possibile archiviare un'istanza di DLL del parser e quindi utilizzarla per una chiamata di sistema in futuro.</span><span class="sxs-lookup"><span data-stu-id="e56e8-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="e56e8-130">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="e56e8-130">For information on</span></span>                                        | <span data-ttu-id="e56e8-131">Vedere</span><span class="sxs-lookup"><span data-stu-id="e56e8-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e56e8-132">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="e56e8-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="e56e8-133">Parser</span><span class="sxs-lookup"><span data-stu-id="e56e8-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="e56e8-134">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="e56e8-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="e56e8-135">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="e56e8-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="e56e8-136">Come implementare **DllMain**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="e56e8-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="e56e8-137">Implementazione di DllMain</span><span class="sxs-lookup"><span data-stu-id="e56e8-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="e56e8-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e56e8-138">Requirements</span></span>



| <span data-ttu-id="e56e8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e56e8-139">Requirement</span></span> | <span data-ttu-id="e56e8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e56e8-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e56e8-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e56e8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e56e8-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e56e8-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e56e8-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e56e8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e56e8-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e56e8-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e56e8-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e56e8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56e8-146"><dt>Elabora. h</dt></span><span class="sxs-lookup"><span data-stu-id="e56e8-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56e8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e56e8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56e8-148">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="e56e8-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="e56e8-149">DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="e56e8-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="e56e8-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="e56e8-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

