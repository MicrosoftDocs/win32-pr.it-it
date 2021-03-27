---
description: Registra i servizi di Dynamic Data Exchange della shell (DDE) nel processo corrente, notificando al sistema che il processo corrente desidera ospitare oggetti DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980442"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="2af9a-103">ShellDDEInit (funzione)</span><span class="sxs-lookup"><span data-stu-id="2af9a-103">ShellDDEInit function</span></span>

<span data-ttu-id="2af9a-104">Registra i servizi di Dynamic Data Exchange della shell (DDE) nel processo corrente, notificando al sistema che il processo corrente desidera ospitare oggetti DDE.</span><span class="sxs-lookup"><span data-stu-id="2af9a-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2af9a-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="2af9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2af9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af9a-107">*init* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2af9a-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af9a-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="2af9a-108">Type: **BOOL**</span></span>

<span data-ttu-id="2af9a-109">**True** per registrare il processo corrente come host DDE; **False** per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2af9a-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af9a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2af9a-110">Return value</span></span>

<span data-ttu-id="2af9a-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2af9a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2af9a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2af9a-112">Remarks</span></span>

<span data-ttu-id="2af9a-113">Il processo che chiama questa funzione funge da Shell e viene usato per visualizzare il contenuto delle cartelle aperte con il verbo ' Open ' di [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="2af9a-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="2af9a-114">Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale.</span><span class="sxs-lookup"><span data-stu-id="2af9a-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="2af9a-115">Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Shdocvw.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="2af9a-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="2af9a-116">Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale di funzione 118 per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="2af9a-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2af9a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2af9a-117">Requirements</span></span>



| <span data-ttu-id="2af9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2af9a-118">Requirement</span></span> | <span data-ttu-id="2af9a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2af9a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af9a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2af9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2af9a-121">Solo app desktop Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="2af9a-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2af9a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2af9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2af9a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2af9a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2af9a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2af9a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2af9a-125"><dt>Shdocvw.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2af9a-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
