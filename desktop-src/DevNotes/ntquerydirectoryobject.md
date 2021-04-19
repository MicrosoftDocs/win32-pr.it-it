---
description: Recupera le informazioni sull'oggetto directory specificato.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326092"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="8f484-103">NtQueryDirectoryObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="8f484-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="8f484-104">\[Questa funzione può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8f484-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8f484-105">Recupera le informazioni sull'oggetto directory specificato.</span><span class="sxs-lookup"><span data-stu-id="8f484-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f484-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f484-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="8f484-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f484-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f484-108">*DirectoryHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f484-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-109">Handle per l'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="8f484-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-110">*Buffer* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8f484-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-111">Puntatore a un buffer che riceve le informazioni sulla directory.</span><span class="sxs-lookup"><span data-stu-id="8f484-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="8f484-112">Questo buffer riceve una o più strutture di **\_ \_ informazioni di directory degli oggetti** , l'ultima è **null**, seguita da stringhe che contengono i nomi delle voci di directory.</span><span class="sxs-lookup"><span data-stu-id="8f484-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="8f484-113">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8f484-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-114">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f484-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-115">Dimensioni in byte del buffer di output fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8f484-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-116">*ReturnSingleEntry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f484-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-117">Indica se la funzione deve restituire solo una singola voce.</span><span class="sxs-lookup"><span data-stu-id="8f484-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-118">*RestartScan* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f484-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-119">Indica se riavviare l'analisi o continuare l'enumerazione utilizzando le informazioni passate nel parametro di *contesto* .</span><span class="sxs-lookup"><span data-stu-id="8f484-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-120">*Contesto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8f484-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-121">Contesto di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="8f484-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="8f484-122">*ReturnLength* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8f484-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f484-123">Puntatore a una variabile che riceve la lunghezza delle informazioni di directory restituite nel buffer di output, in byte.</span><span class="sxs-lookup"><span data-stu-id="8f484-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f484-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f484-124">Return value</span></span>

<span data-ttu-id="8f484-125">La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="8f484-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f484-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f484-126">Remarks</span></span>

<span data-ttu-id="8f484-127">Di seguito è riportata la definizione della struttura delle **\_ \_ informazioni della directory degli oggetti** .</span><span class="sxs-lookup"><span data-stu-id="8f484-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="8f484-128">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8f484-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f484-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f484-129">Requirements</span></span>



| <span data-ttu-id="8f484-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f484-130">Requirement</span></span> | <span data-ttu-id="8f484-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8f484-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8f484-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8f484-132">DLL</span></span><br/> | <dl> <span data-ttu-id="8f484-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f484-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f484-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f484-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f484-135">**NtOpenDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="8f484-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
