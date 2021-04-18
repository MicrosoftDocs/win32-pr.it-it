---
title: TLSDisconnectFromServer (funzione)
description: Chiude un handle aperto per un server licenze Desktop remoto.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione TLSDisconnectFromServer
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302594"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="0b923-104">TLSDisconnectFromServer (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b923-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="0b923-105">Chiude un handle aperto per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0b923-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="0b923-106">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="0b923-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="0b923-107">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="0b923-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0b923-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b923-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="0b923-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b923-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b923-110">*hHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b923-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b923-111">Handle per un server licenze Desktop remoto aperto da una chiamata alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0b923-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b923-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b923-112">Return value</span></span>

<span data-ttu-id="0b923-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0b923-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b923-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b923-114">Remarks</span></span>

<span data-ttu-id="0b923-115">Chiamare la funzione **TLSDisconnectFromServer** come parte della routine di pulizia del programma per chiudere tutti gli handle del server aperti dalle chiamate alla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0b923-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b923-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b923-116">Requirements</span></span>



| <span data-ttu-id="0b923-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b923-117">Requirement</span></span> | <span data-ttu-id="0b923-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0b923-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b923-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b923-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b923-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b923-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b923-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b923-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b923-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b923-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b923-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0b923-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b923-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b923-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b923-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b923-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b923-126">**\_handle TLS**</span><span class="sxs-lookup"><span data-stu-id="0b923-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="0b923-127">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="0b923-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

