---
title: CleanupCredentialCache (funzione)
description: Implementato da determinati provider di supporto per la sicurezza (SSP) per scaricare la cache delle credenziali SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Funzione CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119034"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="0b4df-104">CleanupCredentialCache (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b4df-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="0b4df-105">La funzione **CleanupCredentialCache** viene implementata da determinati provider di supporto della sicurezza (SSP) per scaricare la cache delle credenziali SSP.</span><span class="sxs-lookup"><span data-stu-id="0b4df-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4df-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b4df-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="0b4df-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b4df-107">Parameters</span></span>

<span data-ttu-id="0b4df-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="0b4df-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b4df-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b4df-109">Return value</span></span>

<span data-ttu-id="0b4df-110">**True** se la funzione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0b4df-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b4df-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b4df-111">Remarks</span></span>

<span data-ttu-id="0b4df-112">La funzione **CleanupCredentialCache** viene implementata dai provider di servizi condivisi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b4df-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="0b4df-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="0b4df-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="0b4df-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="0b4df-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="0b4df-115">L'implementazione di **CleanupCredentialCache** da questi SSP restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="0b4df-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="0b4df-116">Prima di provare a ottenere un handle del modulo per esportare **CleanupCredentialCache**, l'applicazione deve verificare che il provider di servizi condivisi che è stato caricato sia uno dei SSP noti che implementa la funzione **CleanupCredentialCache** .</span><span class="sxs-lookup"><span data-stu-id="0b4df-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="0b4df-117">Per scaricare la cache delle credenziali SSP, l'applicazione deve ottenere un handle del modulo per il provider di servizi condivisi chiamando la funzione [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="0b4df-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="0b4df-118">Dopo aver ottenuto il modulo, l'applicazione deve esportare la funzione **CleanupCredentialCache** implementata dal provider di servizi condivisi chiamando la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , passando il modulo restituito da **GetModuleHandle** e **CleanupCredentialCache** come parametri di input.</span><span class="sxs-lookup"><span data-stu-id="0b4df-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="0b4df-119">Come tutti gli altri aspetti dell'API WinINet, questa funzione non può essere chiamata in modo sicuro da DllMain o dai costruttori e dai distruttori di oggetti globali.</span><span class="sxs-lookup"><span data-stu-id="0b4df-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="0b4df-120">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="0b4df-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="0b4df-121">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="0b4df-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0b4df-122">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0b4df-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b4df-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b4df-123">Requirements</span></span>



| <span data-ttu-id="0b4df-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b4df-124">Requirement</span></span> | <span data-ttu-id="0b4df-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0b4df-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4df-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b4df-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b4df-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b4df-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="0b4df-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b4df-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b4df-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b4df-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="0b4df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0b4df-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b4df-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b4df-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

