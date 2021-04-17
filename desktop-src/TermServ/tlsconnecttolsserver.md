---
title: TLSConnectToLsServer (funzione)
description: Apre un handle per il server licenze Desktop remoto specificato.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSConnectToLsServer
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400727"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="16929-104">TLSConnectToLsServer (funzione)</span><span class="sxs-lookup"><span data-stu-id="16929-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="16929-105">Apre un handle per il server licenze Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="16929-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="16929-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="16929-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="16929-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="16929-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="16929-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16929-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="16929-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="16929-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16929-110">*pszLsServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16929-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16929-111">Puntatore a una stringa con terminazione **null** che specifica il nome NetBIOS del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16929-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="16929-112">Se il valore di questo parametro è **null**, il server specificato è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="16929-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16929-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16929-113">Return value</span></span>

<span data-ttu-id="16929-114">Se la funzione ha esito positivo, il valore restituito è un handle per il server specificato.</span><span class="sxs-lookup"><span data-stu-id="16929-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="16929-115">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="16929-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="16929-116">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="16929-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="16929-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="16929-117">Remarks</span></span>

<span data-ttu-id="16929-118">Al termine dell'utilizzo dell'handle restituito dalla funzione **TLSConnectToLsServer** , rilasciarlo chiamando la funzione [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .</span><span class="sxs-lookup"><span data-stu-id="16929-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16929-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16929-119">Requirements</span></span>



| <span data-ttu-id="16929-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16929-120">Requirement</span></span> | <span data-ttu-id="16929-121">Valore</span><span class="sxs-lookup"><span data-stu-id="16929-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16929-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16929-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16929-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16929-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16929-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16929-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16929-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16929-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16929-126">DLL</span><span class="sxs-lookup"><span data-stu-id="16929-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16929-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16929-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16929-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16929-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16929-129">**\_handle TLS**</span><span class="sxs-lookup"><span data-stu-id="16929-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="16929-130">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="16929-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

