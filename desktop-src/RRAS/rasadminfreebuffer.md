---
title: Funzione RasAdminFreeBuffer (rassapi. h)
description: La funzione RasAdminFreeBuffer libera la memoria allocata da RAS per conto del chiamante.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RAS funzione RasAdminFreeBuffer
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333973"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="99d9e-104">RasAdminFreeBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="99d9e-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="99d9e-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="99d9e-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="99d9e-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="99d9e-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="99d9e-107">Le applicazioni devono utilizzare la funzione [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]</span><span class="sxs-lookup"><span data-stu-id="99d9e-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="99d9e-108">La funzione **RasAdminFreeBuffer** libera la memoria allocata da RAS per conto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="99d9e-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99d9e-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="99d9e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="99d9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99d9e-111">*Puntatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99d9e-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99d9e-112">Puntatore al buffer da liberare.</span><span class="sxs-lookup"><span data-stu-id="99d9e-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99d9e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99d9e-113">Return value</span></span>

<span data-ttu-id="99d9e-114">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="99d9e-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="99d9e-115">Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="99d9e-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="99d9e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="99d9e-116">Value</span></span>                                                                                                    | <span data-ttu-id="99d9e-117">Significato</span><span class="sxs-lookup"><span data-stu-id="99d9e-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="99d9e-118"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99d9e-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="99d9e-119">Il parametro del *puntatore* non è valido.</span><span class="sxs-lookup"><span data-stu-id="99d9e-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="99d9e-120">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="99d9e-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="99d9e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="99d9e-121">Remarks</span></span>

<span data-ttu-id="99d9e-122">Utilizzare la funzione **RasAdminFreeBuffer** per liberare i buffer allocati dalle funzioni [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="99d9e-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="99d9e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99d9e-123">Requirements</span></span>



| <span data-ttu-id="99d9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="99d9e-124">Requirement</span></span> | <span data-ttu-id="99d9e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="99d9e-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99d9e-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="99d9e-126">End of client support</span></span><br/> | <span data-ttu-id="99d9e-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="99d9e-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="99d9e-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="99d9e-128">End of server support</span></span><br/> | <span data-ttu-id="99d9e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99d9e-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="99d9e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99d9e-130">Header</span></span><br/>                | <dl> <span data-ttu-id="99d9e-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99d9e-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="99d9e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="99d9e-132">Library</span></span><br/>               | <dl> <span data-ttu-id="99d9e-133"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99d9e-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="99d9e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="99d9e-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="99d9e-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99d9e-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99d9e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99d9e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d9e-137">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="99d9e-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="99d9e-138">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="99d9e-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="99d9e-139">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="99d9e-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="99d9e-140">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="99d9e-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

