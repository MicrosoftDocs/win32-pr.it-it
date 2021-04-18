---
title: Funzione RasAdminPortClearStatistics (rassapi. h)
description: La funzione RasAdminPortClearStatistics Reimposta i contatori che rappresentano le varie statistiche restituite dalla funzione RasAdminPortGetInfo nella struttura delle \_ statistiche della porta RAS \_ . I contatori vengono reimpostati su zero e avviano l'accumulo.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RAS funzione RasAdminPortClearStatistics
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327902"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="26e9d-105">RasAdminPortClearStatistics (funzione)</span><span class="sxs-lookup"><span data-stu-id="26e9d-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="26e9d-106">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="26e9d-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="26e9d-107">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="26e9d-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="26e9d-108">Le applicazioni devono utilizzare la funzione [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]</span><span class="sxs-lookup"><span data-stu-id="26e9d-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="26e9d-109">La funzione **RasAdminPortClearStatistics** Reimposta i contatori che rappresentano le varie statistiche restituite dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) nella struttura [**delle \_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) .</span><span class="sxs-lookup"><span data-stu-id="26e9d-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="26e9d-110">I contatori vengono reimpostati su zero e avviano l'accumulo.</span><span class="sxs-lookup"><span data-stu-id="26e9d-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e9d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26e9d-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="26e9d-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="26e9d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e9d-113">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26e9d-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e9d-114">Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS.</span><span class="sxs-lookup"><span data-stu-id="26e9d-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="26e9d-115">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="26e9d-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="26e9d-116">*lpszPort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26e9d-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e9d-117">Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta nel server.</span><span class="sxs-lookup"><span data-stu-id="26e9d-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e9d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26e9d-118">Return value</span></span>

<span data-ttu-id="26e9d-119">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="26e9d-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="26e9d-120">Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="26e9d-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="26e9d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="26e9d-121">Value</span></span>                                                                                                 | <span data-ttu-id="26e9d-122">Significato</span><span class="sxs-lookup"><span data-stu-id="26e9d-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="26e9d-123"><dt>**ERRORE \_ dev \_ non \_ esiste**</dt></span><span class="sxs-lookup"><span data-stu-id="26e9d-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="26e9d-124">La porta specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="26e9d-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="26e9d-125">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="26e9d-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="26e9d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="26e9d-126">Remarks</span></span>

<span data-ttu-id="26e9d-127">La funzione **RasAdminPortClearStatistics** Cancella le statistiche sul server, non localmente all'interno dell'applicazione che effettua la chiamata.</span><span class="sxs-lookup"><span data-stu-id="26e9d-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="26e9d-128">Ciò significa che le statistiche vengono reimpostate anche per qualsiasi altra applicazione che sta monitorando la porta specificata.</span><span class="sxs-lookup"><span data-stu-id="26e9d-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="26e9d-129">Se la porta *lpszPort* fa parte di una connessione a più collegamenti, **RasAdminPortClearStatistics** Reimposta le statistiche per la porta specificata, la funzione Reimposta anche le statistiche cumulative per la connessione a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="26e9d-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="26e9d-130">Tuttavia, la funzione non influisce sulle singole statistiche per le altre porte che fanno parte della connessione a più collegamenti.</span><span class="sxs-lookup"><span data-stu-id="26e9d-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e9d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26e9d-131">Requirements</span></span>



| <span data-ttu-id="26e9d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e9d-132">Requirement</span></span> | <span data-ttu-id="26e9d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="26e9d-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e9d-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="26e9d-134">End of client support</span></span><br/> | <span data-ttu-id="26e9d-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26e9d-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="26e9d-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="26e9d-136">End of server support</span></span><br/> | <span data-ttu-id="26e9d-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26e9d-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="26e9d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e9d-138">Header</span></span><br/>                | <dl> <span data-ttu-id="26e9d-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e9d-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="26e9d-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="26e9d-140">Library</span></span><br/>               | <dl> <span data-ttu-id="26e9d-141"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26e9d-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="26e9d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="26e9d-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="26e9d-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e9d-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e9d-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26e9d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e9d-145">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="26e9d-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="26e9d-146">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="26e9d-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="26e9d-147">**\_statistiche porta \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="26e9d-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="26e9d-148">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="26e9d-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

