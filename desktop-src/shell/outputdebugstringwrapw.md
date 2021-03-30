---
description: Invia una stringa Unicode al debugger per la visualizzazione.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Funzione OutputDebugStringWrapW (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994821"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="b2e47-103">OutputDebugStringWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="b2e47-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="b2e47-104">\[Questa funzione è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2e47-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="b2e47-105">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b2e47-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="b2e47-106">Usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="b2e47-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="b2e47-107">Invia una stringa Unicode al debugger per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b2e47-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="b2e47-108">**OutputDebugStringWrapW** è un wrapper per la funzione **OutputDebugStringW** .</span><span class="sxs-lookup"><span data-stu-id="b2e47-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="b2e47-109">Per ulteriori note sull'utilizzo, vedere la pagina [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .</span><span class="sxs-lookup"><span data-stu-id="b2e47-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b2e47-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2e47-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="b2e47-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2e47-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e47-112">*lpOutputString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2e47-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e47-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b2e47-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b2e47-114">Puntatore alla stringa Unicode con terminazione null da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="b2e47-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e47-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2e47-115">Return value</span></span>

<span data-ttu-id="b2e47-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b2e47-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e47-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2e47-117">Remarks</span></span>

<span data-ttu-id="b2e47-118">**OutputDebugStringWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2e47-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="b2e47-119">Il metodo preferito consiste nell'usare [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="b2e47-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="b2e47-120">**OutputDebugStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 115.</span><span class="sxs-lookup"><span data-stu-id="b2e47-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="b2e47-121">Se l'applicazione non dispone di un debugger, il debugger di sistema Visualizza la stringa.</span><span class="sxs-lookup"><span data-stu-id="b2e47-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="b2e47-122">Se l'applicazione non dispone di un debugger e il debugger di sistema non è attivo, **OutputDebugStringWrapW** non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="b2e47-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e47-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2e47-123">Requirements</span></span>



| <span data-ttu-id="b2e47-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e47-124">Requirement</span></span> | <span data-ttu-id="b2e47-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b2e47-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e47-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e47-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e47-127">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2e47-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2e47-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e47-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e47-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2e47-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b2e47-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2e47-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e47-131"><dt>Shlwapip. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e47-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="b2e47-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e47-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e47-133"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b2e47-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e47-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2e47-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e47-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="b2e47-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
