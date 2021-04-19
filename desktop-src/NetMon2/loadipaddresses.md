---
description: La funzione LoadIPAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Funzione LoadIPAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319938"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="05a82-103">LoadIPAddresses (funzione)</span><span class="sxs-lookup"><span data-stu-id="05a82-103">LoadIPAddresses function</span></span>

<span data-ttu-id="05a82-104">La funzione **LoadIPAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="05a82-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05a82-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="05a82-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05a82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a82-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05a82-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a82-108">Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="05a82-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="05a82-109">*pVarName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05a82-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a82-110">Puntatore al nome della variabile nella stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="05a82-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="05a82-111">*ppAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05a82-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05a82-112">Puntatore a un puntatore a una matrice di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="05a82-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="05a82-113">Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, la funzione alloca spazio sufficiente e archivia tutti gli indirizzi IP come matrice.</span><span class="sxs-lookup"><span data-stu-id="05a82-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="05a82-114">*pNumAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05a82-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05a82-115">Puntatore alla variabile **DWORD** impostata sul numero di indirizzi IP ricavati dalla stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="05a82-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a82-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05a82-116">Return value</span></span>

<span data-ttu-id="05a82-117">Se la funzione ha esito positivo (il nome della variabile è stato trovato e presenta una stringa di lunghezza diversa da zero che rappresenta gli indirizzi IP), il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="05a82-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="05a82-118">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="05a82-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a82-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="05a82-119">Remarks</span></span>

<span data-ttu-id="05a82-120">Gli indirizzi IP devono essere nel formato x. x.x. x, ad esempio 127.0.0.1.</span><span class="sxs-lookup"><span data-stu-id="05a82-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="05a82-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05a82-121">Requirements</span></span>



| <span data-ttu-id="05a82-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a82-122">Requirement</span></span> | <span data-ttu-id="05a82-123">Valore</span><span class="sxs-lookup"><span data-stu-id="05a82-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05a82-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05a82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05a82-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="05a82-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="05a82-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05a82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05a82-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="05a82-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05a82-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05a82-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a82-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a82-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="05a82-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="05a82-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="05a82-131"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05a82-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="05a82-132">DLL</span><span class="sxs-lookup"><span data-stu-id="05a82-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05a82-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05a82-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




