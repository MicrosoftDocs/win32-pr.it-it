---
description: La funzione LoadIPXAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Funzione LoadIPXAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233302"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="b9ff3-103">LoadIPXAddresses (funzione)</span><span class="sxs-lookup"><span data-stu-id="b9ff3-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="b9ff3-104">La funzione **LoadIPXAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi IPX tratto da una variabile di stringa di configurazione HTML.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ff3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9ff3-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="b9ff3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ff3-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff3-108">Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="b9ff3-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b9ff3-109">*pVarName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff3-110">Puntatore al nome della variabile nella stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="b9ff3-111">*ppAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff3-112">Puntatore a un puntatore a una matrice di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="b9ff3-113">Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, viene allocato spazio sufficiente (usando **HeapAllocMemory**) e tutti gli indirizzi IPX vengono archiviati come matrice.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="b9ff3-114">*pNumAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff3-115">Puntatore alla variabile **DWORD** impostata sul numero di indirizzi IPX ricavati dalla stringa di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ff3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9ff3-116">Return value</span></span>

<span data-ttu-id="b9ff3-117">Se la funzione ha esito positivo (il nome della variabile è stato trovato e ha una stringa di lunghezza non zero che rappresentava gli indirizzi IPX), il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="b9ff3-118">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b9ff3-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ff3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9ff3-119">Requirements</span></span>



| <span data-ttu-id="b9ff3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ff3-120">Requirement</span></span> | <span data-ttu-id="b9ff3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b9ff3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ff3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9ff3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ff3-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b9ff3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9ff3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ff3-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9ff3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b9ff3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9ff3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ff3-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff3-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b9ff3-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9ff3-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9ff3-129"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff3-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9ff3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b9ff3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9ff3-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff3-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




