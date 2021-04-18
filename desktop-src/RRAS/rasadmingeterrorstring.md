---
title: Funzione RasAdminGetErrorString (rassapi. h)
description: La funzione RasAdminGetErrorString recupera una stringa di messaggio che corrisponde a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RAS funzione RasAdminGetErrorString
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327906"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="b5c91-104">RasAdminGetErrorString (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5c91-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="b5c91-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b5c91-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b5c91-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b5c91-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b5c91-107">Le applicazioni devono utilizzare la funzione [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]</span><span class="sxs-lookup"><span data-stu-id="b5c91-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="b5c91-108">La funzione **RasAdminGetErrorString** recupera una stringa di messaggio che corrisponde a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RASADMIN).</span><span class="sxs-lookup"><span data-stu-id="b5c91-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="b5c91-109">Queste stringhe di messaggio vengono recuperate dal Rasmsg.dll installato come parte di RAS.</span><span class="sxs-lookup"><span data-stu-id="b5c91-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c91-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c91-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="b5c91-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5c91-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c91-112">*ResourceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5c91-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c91-113">Specifica un codice di errore restituito da una delle funzioni RasAdmin.</span><span class="sxs-lookup"><span data-stu-id="b5c91-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="b5c91-114">Questo valore deve essere compreso nell'intervallo di codici di errore da RASBASE a RASBASEEND.</span><span class="sxs-lookup"><span data-stu-id="b5c91-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="b5c91-115">Questi sono definiti in Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="b5c91-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="b5c91-116">*lpszString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5c91-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c91-117">Puntatore a un buffer che riceve il messaggio di errore corrispondente al codice di errore specificato.</span><span class="sxs-lookup"><span data-stu-id="b5c91-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="b5c91-118">*InBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5c91-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c91-119">Specifica la dimensione, in caratteri, del buffer *lpszString* .</span><span class="sxs-lookup"><span data-stu-id="b5c91-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="b5c91-120">I messaggi di errore sono in genere di 80 caratteri o meno. una dimensione del buffer di 512 caratteri è sempre adeguata.</span><span class="sxs-lookup"><span data-stu-id="b5c91-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c91-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5c91-121">Return value</span></span>

<span data-ttu-id="b5c91-122">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b5c91-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b5c91-123">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="b5c91-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="b5c91-124">Questo valore può essere un ultimo valore di errore impostato dalle funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)o [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) . oppure può essere uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5c91-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="b5c91-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b5c91-125">Value</span></span>                                                                                                      | <span data-ttu-id="b5c91-126">Significato</span><span class="sxs-lookup"><span data-stu-id="b5c91-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5c91-127"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c91-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="b5c91-128">I parametri *resourceId* o *lpszString* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="b5c91-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="b5c91-129"><dt>**ERRORE \_ buffer insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c91-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="b5c91-130">La dimensione specificata dal parametro *InBufSize* è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="b5c91-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="b5c91-131">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b5c91-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c91-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5c91-132">Remarks</span></span>

<span data-ttu-id="b5c91-133">Le funzioni RasAdmin possono restituire codici di errore non compresi nell'intervallo supportato dalla funzione **RasAdminGetErrorString** .</span><span class="sxs-lookup"><span data-stu-id="b5c91-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="b5c91-134">Ad esempio, le funzioni RasAdmin possono restituire codici di errore definiti in Lmerr. h e Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b5c91-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="b5c91-135">Prima di chiamare **RasAdminGetErrorString**, verificare che il codice di errore sia compreso nell'intervallo da rasbase a RASBASEEND, come definito in Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="b5c91-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c91-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5c91-136">Requirements</span></span>



| <span data-ttu-id="b5c91-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c91-137">Requirement</span></span> | <span data-ttu-id="b5c91-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b5c91-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c91-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b5c91-139">End of client support</span></span><br/> | <span data-ttu-id="b5c91-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5c91-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b5c91-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b5c91-141">End of server support</span></span><br/> | <span data-ttu-id="b5c91-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5c91-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b5c91-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5c91-143">Header</span></span><br/>                | <dl> <span data-ttu-id="b5c91-144"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c91-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5c91-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5c91-145">Library</span></span><br/>               | <dl> <span data-ttu-id="b5c91-146"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5c91-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5c91-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b5c91-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b5c91-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5c91-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c91-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5c91-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c91-150">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b5c91-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b5c91-151">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="b5c91-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b5c91-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="b5c91-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="b5c91-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b5c91-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="b5c91-154">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="b5c91-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

