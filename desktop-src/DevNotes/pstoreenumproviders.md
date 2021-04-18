---
description: Ottiene un oggetto enumeratore che può essere utilizzato a sua volta per enumerare i provider di archiviazione protetti attualmente installati nel sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Funzione PStoreEnumProviders (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330961"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="1a3a5-103">PStoreEnumProviders (funzione)</span><span class="sxs-lookup"><span data-stu-id="1a3a5-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="1a3a5-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="1a3a5-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="1a3a5-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="1a3a5-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="1a3a5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="1a3a5-108">Ottiene un oggetto enumeratore che può essere utilizzato a sua volta per enumerare i provider di archiviazione protetti attualmente installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3a5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a3a5-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="1a3a5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a3a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3a5-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1a3a5-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3a5-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a3a5-113">*ppenum*</span><span class="sxs-lookup"><span data-stu-id="1a3a5-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3a5-114">Puntatore a un puntatore a un'interfaccia [**IEnumPStoreProviders**](ienumpstoreproviders.md) che può essere utilizzata per enumerare i provider installati.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3a5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a3a5-115">Return value</span></span>

<span data-ttu-id="1a3a5-116">Questa funzione restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3a5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a3a5-117">Remarks</span></span>

<span data-ttu-id="1a3a5-118">Il componente di archiviazione protetta dispone di un'architettura basata su provider.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="1a3a5-119">Le applicazioni che usano l'archiviazione protetta possono specificare quali provider installati usare durante l'archiviazione e il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="1a3a5-120">La funzione **PStoreEnumProviders** viene utilizzata per enumerare i provider di archiviazione protetti installati.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="1a3a5-121">Ogni provider viene identificato da un identificatore univoco globale (GUID).</span><span class="sxs-lookup"><span data-stu-id="1a3a5-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="1a3a5-122">Fino a questo momento, è già stato scritto un solo provider di archiviazione protetto.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="1a3a5-123">Dato che il servizio di archiviazione protetto è attualmente deprecato, è molto improbabile che vengano generati altri provider.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="1a3a5-124">Di conseguenza, questa funzione non deve essere usata per alcuno scopo.</span><span class="sxs-lookup"><span data-stu-id="1a3a5-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="1a3a5-125">A questa funzione non è associata alcuna libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1a3a5-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3a5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a3a5-126">Requirements</span></span>



| <span data-ttu-id="1a3a5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3a5-127">Requirement</span></span> | <span data-ttu-id="1a3a5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1a3a5-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3a5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a3a5-129">Header</span></span><br/> | <dl> <span data-ttu-id="1a3a5-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a3a5-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="1a3a5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1a3a5-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="1a3a5-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a3a5-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3a5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a3a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3a5-134">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="1a3a5-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
