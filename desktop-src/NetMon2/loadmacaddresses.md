---
description: La funzione LoadMACAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi MAC con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Funzione LoadMACAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526767"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="cd409-103">LoadMACAddresses (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd409-103">LoadMACAddresses function</span></span>

<span data-ttu-id="cd409-104">La funzione **LoadMACAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi Mac con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="cd409-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd409-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd409-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="cd409-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd409-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd409-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd409-108">Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="cd409-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="cd409-109">*pVarName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd409-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd409-110">Puntatore al nome della variabile nella stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="cd409-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="cd409-111">*ppAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd409-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd409-112">Puntatore a un puntatore a una matrice di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="cd409-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="cd409-113">Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, la funzione alloca spazio sufficiente (usando **HeapAllocMemory**) e archivia tutti gli indirizzi Mac come matrice.</span><span class="sxs-lookup"><span data-stu-id="cd409-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="cd409-114">*pNumAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd409-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd409-115">Puntatore alla variabile **DWORD** impostata sul numero di indirizzi Mac ricavati dalla stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="cd409-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd409-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd409-116">Return value</span></span>

<span data-ttu-id="cd409-117">Se la funzione ha esito positivo, (il nome della variabile è stato trovato e presenta una stringa di lunghezza diversa da zero che rappresenta gli indirizzi MAC), il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="cd409-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="cd409-118">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="cd409-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd409-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd409-119">Requirements</span></span>



| <span data-ttu-id="cd409-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd409-120">Requirement</span></span> | <span data-ttu-id="cd409-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cd409-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd409-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd409-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd409-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd409-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd409-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd409-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd409-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd409-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd409-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd409-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd409-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd409-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cd409-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd409-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd409-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd409-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd409-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cd409-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd409-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd409-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




