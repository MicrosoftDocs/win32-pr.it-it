---
description: Apre un collegamento simbolico esistente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329049"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="9a7a6-103">NtOpenSymbolicLinkObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="9a7a6-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="9a7a6-104">\[Questa funzione può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9a7a6-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9a7a6-105">Apre un collegamento simbolico esistente.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a7a6-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="9a7a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a7a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7a6-108">*LinkHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9a7a6-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7a6-109">Handle per l'oggetto collegamento simbolico appena aperto.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="9a7a6-110">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a7a6-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7a6-111">[**\_ Maschera di accesso**](../secauthz/access-mask.md) che specifica l'accesso richiesto all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="9a7a6-112">È tipico utilizzare \_ la lettura generica in modo che sia possibile passare l'handle alla funzione [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7a6-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9a7a6-113">*ObjectAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a7a6-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7a6-114">Attributi per l'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-114">The attributes for the directory object.</span></span> <span data-ttu-id="9a7a6-115">Per inizializzare la struttura degli **\_ attributi dell'oggetto** , usare la macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="9a7a6-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="9a7a6-116">Se il chiamante non è in esecuzione in un contesto del thread di sistema, è necessario specificare il flag di **\_ \_ handle del kernel obj** durante l'inizializzazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="9a7a6-117">Per ulteriori informazioni, vedere la documentazione relativa a questi elementi nella documentazione relativa a WDK.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7a6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a7a6-118">Return value</span></span>

<span data-ttu-id="9a7a6-119">La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="9a7a6-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7a6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a7a6-120">Remarks</span></span>

<span data-ttu-id="9a7a6-121">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9a7a6-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7a6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a7a6-122">Requirements</span></span>



| <span data-ttu-id="9a7a6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7a6-123">Requirement</span></span> | <span data-ttu-id="9a7a6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7a6-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7a6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9a7a6-125">DLL</span></span><br/> | <dl> <span data-ttu-id="9a7a6-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7a6-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7a6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a7a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7a6-128">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="9a7a6-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
