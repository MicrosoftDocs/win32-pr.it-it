---
title: Funzione RasAdminPortGetInfo (rassapi. h)
description: La funzione RasAdminPortGetInfo recupera le informazioni su una porta specificata in un server specificato.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RAS funzione RasAdminPortGetInfo
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330765"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="b405e-104">RasAdminPortGetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="b405e-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="b405e-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b405e-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b405e-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b405e-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b405e-107">Le applicazioni devono utilizzare la funzione [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="b405e-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="b405e-108">La funzione **RasAdminPortGetInfo** recupera le informazioni su una porta specificata in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="b405e-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b405e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b405e-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="b405e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b405e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b405e-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b405e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b405e-112">Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS.</span><span class="sxs-lookup"><span data-stu-id="b405e-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="b405e-113">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="b405e-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="b405e-114">*lpszPort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b405e-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b405e-115">Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta nel server.</span><span class="sxs-lookup"><span data-stu-id="b405e-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="b405e-116">*pRasPort1* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b405e-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b405e-117">Puntatore alla struttura [**della \_ porta RAS \_ 1**](ras-port-1-str.md) che la funzione compila con informazioni sullo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="b405e-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="b405e-118">*pRasStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b405e-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b405e-119">Puntatore alla struttura [**delle \_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) che la funzione compila con le statistiche sulla porta.</span><span class="sxs-lookup"><span data-stu-id="b405e-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="b405e-120">*ppRasParams* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b405e-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b405e-121">Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) .</span><span class="sxs-lookup"><span data-stu-id="b405e-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="b405e-122">Ogni struttura contiene il nome di una chiave specifica del supporto, ad esempio MAXCONNECTBPS, e il relativo valore associato.</span><span class="sxs-lookup"><span data-stu-id="b405e-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="b405e-123">Al termine dell'applicazione, liberare la memoria chiamando la funzione [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b405e-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b405e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b405e-124">Return value</span></span>

<span data-ttu-id="b405e-125">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b405e-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b405e-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.</span><span class="sxs-lookup"><span data-stu-id="b405e-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="b405e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b405e-127">Value</span></span>                                                                                                     | <span data-ttu-id="b405e-128">Significato</span><span class="sxs-lookup"><span data-stu-id="b405e-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b405e-129"><dt>**ERRORE \_ dev \_ non \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="b405e-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="b405e-130">La porta specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="b405e-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b405e-131"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b405e-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="b405e-132">Memoria insufficiente per allocare un buffer per la matrice *ppRasParams* .</span><span class="sxs-lookup"><span data-stu-id="b405e-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="b405e-133">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b405e-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="b405e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b405e-134">Requirements</span></span>



| <span data-ttu-id="b405e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b405e-135">Requirement</span></span> | <span data-ttu-id="b405e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b405e-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b405e-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b405e-137">End of client support</span></span><br/> | <span data-ttu-id="b405e-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b405e-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b405e-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b405e-139">End of server support</span></span><br/> | <span data-ttu-id="b405e-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b405e-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b405e-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b405e-141">Header</span></span><br/>                | <dl> <span data-ttu-id="b405e-142"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b405e-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b405e-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="b405e-143">Library</span></span><br/>               | <dl> <span data-ttu-id="b405e-144"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b405e-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b405e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b405e-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b405e-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b405e-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b405e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b405e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b405e-148">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b405e-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b405e-149">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="b405e-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b405e-150">**\_parametri RAS**</span><span class="sxs-lookup"><span data-stu-id="b405e-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="b405e-151">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b405e-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="b405e-152">**\_statistiche porta \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="b405e-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="b405e-153">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="b405e-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

