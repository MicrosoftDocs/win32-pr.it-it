---
description: Apre un handle per un oggetto thread con l'accesso specificato.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328276"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="d5c1d-103">NtOpenThread (funzione)</span><span class="sxs-lookup"><span data-stu-id="d5c1d-103">NtOpenThread function</span></span>

<span data-ttu-id="d5c1d-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="d5c1d-105">Usare invece la funzione [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]</span><span class="sxs-lookup"><span data-stu-id="d5c1d-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="d5c1d-106">Apre un handle per un oggetto thread con l'accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5c1d-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="d5c1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5c1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c1d-109">*ThreadHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5c1d-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1d-110">Puntatore a una variabile che riceve l'handle dell'oggetto thread.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="d5c1d-111">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5c1d-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1d-112">Tipo di dati di una [**\_ maschera di accesso**](../secauthz/access-mask-format.md) che fornisce i tipi di accesso desiderati per l'oggetto thread.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="d5c1d-113">*ObjectAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5c1d-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1d-114">Puntatore a una struttura [degli \_ attributi dell'oggetto](https://msdn.microsoft.com/library/aa491657.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d5c1d-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="d5c1d-115">Il membro **ObjectName** di questa struttura deve essere null.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="d5c1d-116">**Windows Server 2003 e Windows XP:** Il membro **ObjectName** di questa struttura può puntare a un nome di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="d5c1d-117">Se **ObjectName** non è null, il parametro *ClientID* deve essere null.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="d5c1d-118">*ClientID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5c1d-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1d-119">Puntatore a una struttura **di \_ ID client** che identifica il thread di cui deve essere aperto il thread.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="d5c1d-120">**Windows Server 2003 e Windows XP:** Puntatore a una struttura **di \_ ID client** che identifica il thread di cui deve essere aperto il thread.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="d5c1d-121">Questo parametro può essere NULL.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-121">This parameter can be NULL.</span></span> <span data-ttu-id="d5c1d-122">Se questo parametro non è NULL, il membro **ObjectName** della struttura a cui punta il parametro *OBJECTATTRIBUTES* deve essere null.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c1d-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5c1d-123">Return value</span></span>

<span data-ttu-id="d5c1d-124">Restituisce un codice **NTSTATUS** o Error.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="d5c1d-125">I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c1d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5c1d-126">Remarks</span></span>

<span data-ttu-id="d5c1d-127">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-127">This function has no associated header file.</span></span> <span data-ttu-id="d5c1d-128">La libreria di importazione associata, Ntdll. lib è disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="d5c1d-129">È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="d5c1d-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c1d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5c1d-130">Requirements</span></span>



| <span data-ttu-id="d5c1d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c1d-131">Requirement</span></span> | <span data-ttu-id="d5c1d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d5c1d-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c1d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c1d-133">DLL</span></span><br/> | <dl> <span data-ttu-id="d5c1d-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c1d-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
