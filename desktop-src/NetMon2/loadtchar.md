---
description: La funzione LoadTCHAR viene chiamata dai monitoraggi per impostare una variabile di stringa su una stringa eseguita da una stringa di configurazione HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Funzione LoadTCHAR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307721"
---
# <a name="loadtchar-function"></a><span data-ttu-id="d6967-103">LoadTCHAR (funzione)</span><span class="sxs-lookup"><span data-stu-id="d6967-103">LoadTCHAR function</span></span>

<span data-ttu-id="d6967-104">La funzione **LoadTCHAR** viene chiamata dai monitoraggi per impostare una variabile di stringa su una stringa eseguita da una stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="d6967-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6967-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6967-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="d6967-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6967-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6967-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6967-108">Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="d6967-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d6967-109">*pVarName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6967-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6967-110">Puntatore al nome della variabile nella stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="d6967-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="d6967-111">*ppszString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d6967-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6967-112">Puntatore a un puntatore di stringa.</span><span class="sxs-lookup"><span data-stu-id="d6967-112">Pointer to a string pointer.</span></span> <span data-ttu-id="d6967-113">Se viene trovato il nome della variabile richiesta, la stringa viene allocata e assegnata a questo puntatore.</span><span class="sxs-lookup"><span data-stu-id="d6967-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="d6967-114">È responsabilità dell'utente liberare la memoria associata alla stringa.</span><span class="sxs-lookup"><span data-stu-id="d6967-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6967-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6967-115">Return value</span></span>

<span data-ttu-id="d6967-116">Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza diversa da zero), il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d6967-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="d6967-117">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d6967-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6967-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6967-118">Requirements</span></span>



| <span data-ttu-id="d6967-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6967-119">Requirement</span></span> | <span data-ttu-id="d6967-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d6967-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6967-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6967-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6967-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6967-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d6967-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6967-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6967-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6967-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6967-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6967-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6967-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6967-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d6967-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6967-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6967-128"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6967-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6967-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d6967-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6967-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6967-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




