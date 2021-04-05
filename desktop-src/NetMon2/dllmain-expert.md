---
description: L'esperto implementa la funzione DllMain. Il sistema operativo chiama DllMain per ottenere un handle per un'istanza dell'esperto.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Funzione di callback dell'esperto DllMain (Process. h)
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
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882914"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="82191-104">Funzione di callback Expert DllMain</span><span class="sxs-lookup"><span data-stu-id="82191-104">DllMain Expert callback function</span></span>

<span data-ttu-id="82191-105">L'esperto implementa la funzione [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="82191-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="82191-106">Il sistema operativo chiama **DllMain** per ottenere un handle per un'istanza dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="82191-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="82191-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82191-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="82191-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="82191-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82191-109">*HINSTANCE* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="82191-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82191-110">Handle per un'istanza dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="82191-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="82191-111">Se l'esperto utilizza l'interfaccia utente di Network Monitor, il valore *HINSTANCE* deve essere archiviato in una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="82191-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="82191-112">Questo approccio è necessario solo quando il valore del parametro *ulReason* è impostato su dll \_ Process \_ Connetti.</span><span class="sxs-lookup"><span data-stu-id="82191-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="82191-113">*ulReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82191-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82191-114">Indicatore del motivo per cui è stata chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="82191-114">Indicator of why the function was called.</span></span> <span data-ttu-id="82191-115">Il valore DLL \_ processo di \_ connessione (che si applica quando la dll viene caricata per la prima volta) indica che l'esperto deve salvare il valore *HINSTANCE* in una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="82191-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="82191-116">Con qualsiasi altro valore, tutte le chiamate alla funzione [**DllMain**](/windows/desktop/Dlls/dllmain) possono essere ignorate.</span><span class="sxs-lookup"><span data-stu-id="82191-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="82191-117">Per un elenco di tutti i flag possibili impostati dal sistema operativo, vedere **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="82191-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="82191-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="82191-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="82191-119">Il parametro non è in uso.</span><span class="sxs-lookup"><span data-stu-id="82191-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82191-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82191-120">Return value</span></span>

<span data-ttu-id="82191-121">Se la funzione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="82191-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="82191-122">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="82191-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="82191-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="82191-123">Remarks</span></span>

<span data-ttu-id="82191-124">Il sistema operativo chiama la funzione dell'esperto **DllMain** quando un processo carica o Scarica la dll di esperti.</span><span class="sxs-lookup"><span data-stu-id="82191-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="82191-125">La funzione Expert **DllMain** deve essere esportata solo se l'esperto dispone di un'interfaccia utente per la visualizzazione della configurazione o dei risultati, quindi solo per la restituzione del valore *HINSTANCE* corretto.</span><span class="sxs-lookup"><span data-stu-id="82191-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="82191-126">La funzione dell'esperto **DllMain** è basata sulla funzione [**DllMain**](/windows/desktop/Dlls/dllmain) della libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="82191-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="82191-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82191-127">Requirements</span></span>



| <span data-ttu-id="82191-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="82191-128">Requirement</span></span> | <span data-ttu-id="82191-129">Valore</span><span class="sxs-lookup"><span data-stu-id="82191-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82191-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82191-130">Minimum supported client</span></span><br/> | <span data-ttu-id="82191-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82191-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82191-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82191-132">Minimum supported server</span></span><br/> | <span data-ttu-id="82191-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82191-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82191-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82191-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="82191-135"><dt>Elabora. h</dt></span><span class="sxs-lookup"><span data-stu-id="82191-135"><dt>Process.h</dt></span></span> </dl> |



 

