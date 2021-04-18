---
description: Recupera un puntatore a interfaccia a un provider di archiviazione.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Funzione PStoreCreateInstance (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329166"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="ce5f7-103">PStoreCreateInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="ce5f7-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="ce5f7-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ce5f7-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ce5f7-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ce5f7-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ce5f7-108">\[Questa funzione può essere modificata o non disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="ce5f7-109">Usare le funzioni **CryptProtectData** e **CryptUnprotectData** anziché questa funzione.\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="ce5f7-110">Recupera un puntatore a interfaccia a un provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5f7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce5f7-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ce5f7-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce5f7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5f7-113">*ppProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f7-114">Puntatore al puntatore a interfaccia recuperato per il provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="ce5f7-115">Al termine dell'utilizzo dell'interfaccia, decrementare il conteggio dei riferimenti chiamando il relativo metodo [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="ce5f7-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="ce5f7-116">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f7-117">*pProviderID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f7-118">Puntatore al **GUID** che identifica il provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="ce5f7-119">Se questo parametro è **null**, viene utilizzato il provider di archiviazione di base.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f7-120">*mantenuta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f7-121">Riservati deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce5f7-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce5f7-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5f7-123">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5f7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce5f7-124">Return value</span></span>

<span data-ttu-id="ce5f7-125">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ce5f7-126">Il valore **S \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ce5f7-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5f7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce5f7-127">Remarks</span></span>

<span data-ttu-id="ce5f7-128">A questa funzione non è associata alcuna libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ce5f7-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5f7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce5f7-129">Requirements</span></span>



| <span data-ttu-id="ce5f7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce5f7-130">Requirement</span></span> | <span data-ttu-id="ce5f7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ce5f7-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5f7-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce5f7-132">Header</span></span><br/> | <dl> <span data-ttu-id="ce5f7-133"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5f7-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ce5f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ce5f7-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="ce5f7-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce5f7-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5f7-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce5f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5f7-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="ce5f7-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="ce5f7-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="ce5f7-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
