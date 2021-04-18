---
title: Funzione di callback PxeProviderInitialize
description: Un'esportazione da una libreria di collegamento dinamico (DLL) del provider che inizializza il provider e prepara la ricezione delle richieste client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Funzione di callback PxeProviderInitialize servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302404"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="99556-104">Funzione di callback PxeProviderInitialize</span><span class="sxs-lookup"><span data-stu-id="99556-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="99556-105">Un'esportazione da una libreria di collegamento dinamico (DLL) del provider che inizializza il provider e prepara la ricezione delle richieste client.</span><span class="sxs-lookup"><span data-stu-id="99556-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="99556-106">I provider sono necessari per esportare la funzione *PxeProviderInitialize* .</span><span class="sxs-lookup"><span data-stu-id="99556-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="99556-107">Tutti i callback al provider devono essere registrati con una chiamata alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante l'elaborazione di *PxeProviderInitialize*.</span><span class="sxs-lookup"><span data-stu-id="99556-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="99556-108">Alla restituzione di questa funzione, il provider deve essere completamente inizializzato e pronto per l'elaborazione delle richieste client.</span><span class="sxs-lookup"><span data-stu-id="99556-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="99556-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99556-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="99556-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="99556-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99556-111">*hProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99556-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99556-112">Handle per l'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="99556-112">Handle to the provider instance.</span></span> <span data-ttu-id="99556-113">Questo handle deve essere archiviato dal provider e utilizzato nelle chiamate successive.</span><span class="sxs-lookup"><span data-stu-id="99556-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="99556-114">Questo handle è valido fino a quando non viene chiamata la funzione di callback [*PxeProviderShutdown*](pxeprovidershutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="99556-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="99556-115">*hProviderKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99556-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99556-116">Handle per una chiave del registro di sistema in cui devono essere archiviate le informazioni di configurazione del provider.</span><span class="sxs-lookup"><span data-stu-id="99556-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99556-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99556-117">Return value</span></span>

<span data-ttu-id="99556-118">Se l'inizializzazione del provider riesce, il callback dovrebbe restituire l' **errore \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="99556-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="99556-119">In caso di errore, dovrebbe essere restituito un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="99556-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="99556-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99556-120">Requirements</span></span>



| <span data-ttu-id="99556-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="99556-121">Requirement</span></span> | <span data-ttu-id="99556-122">Valore</span><span class="sxs-lookup"><span data-stu-id="99556-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99556-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99556-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99556-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="99556-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="99556-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99556-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99556-126">Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]</span><span class="sxs-lookup"><span data-stu-id="99556-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99556-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99556-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99556-128">Funzioni server di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="99556-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="99556-129">*PxeProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="99556-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





