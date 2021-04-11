---
title: GetPhysicalMonitorDescription (funzione)
description: Ottiene una descrizione di un monitor fisico.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configurazione del monitoraggio della funzione GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119706"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="b1da6-104">GetPhysicalMonitorDescription (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1da6-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1da6-105">Questa funzione viene usata dall'API di configurazione del monitoraggio per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b1da6-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="b1da6-106">Le applicazioni non devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b1da6-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="b1da6-107">Ottiene una descrizione di un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="b1da6-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1da6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1da6-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="b1da6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1da6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1da6-110">*hMonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1da6-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1da6-111">Handle per un monitor fisico.</span><span class="sxs-lookup"><span data-stu-id="b1da6-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b1da6-112">*dwPhysicalMonitorDescriptionSizeInChars* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1da6-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1da6-113">Numero di caratteri nella matrice *szPhysicalMonitorDescription* .</span><span class="sxs-lookup"><span data-stu-id="b1da6-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="b1da6-114">*szPhysicalMonitorDescription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1da6-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1da6-115">Puntatore a una matrice che riceve la descrizione.</span><span class="sxs-lookup"><span data-stu-id="b1da6-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="b1da6-116">Il numero di elementi nella matrice deve essere almeno la **Descrizione della \_ \_ \_ dimensione del monitoraggio fisico**.</span><span class="sxs-lookup"><span data-stu-id="b1da6-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1da6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1da6-117">Return value</span></span>

<span data-ttu-id="b1da6-118">Se il metodo ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="b1da6-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="b1da6-119">In caso contrario, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b1da6-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1da6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1da6-120">Remarks</span></span>

<span data-ttu-id="b1da6-121">Anziché utilizzare questa funzione, le applicazioni devono chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1da6-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="b1da6-122">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="b1da6-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="b1da6-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="b1da6-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="b1da6-124">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b1da6-124">This function has no associated import library.</span></span> <span data-ttu-id="b1da6-125">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b1da6-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1da6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1da6-126">Requirements</span></span>



| <span data-ttu-id="b1da6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1da6-127">Requirement</span></span> | <span data-ttu-id="b1da6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b1da6-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1da6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1da6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b1da6-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1da6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b1da6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1da6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b1da6-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1da6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1da6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b1da6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1da6-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1da6-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1da6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1da6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1da6-136">Monitorare le funzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="b1da6-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

