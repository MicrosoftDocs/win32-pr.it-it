---
title: Funzione RasAdminServerGetInfo (rassapi. h)
description: La funzione RasAdminServerGetInfo ottiene la configurazione del server di un server RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RAS funzione RasAdminServerGetInfo
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330764"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="a2617-104">RasAdminServerGetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="a2617-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="a2617-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="a2617-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="a2617-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2617-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="a2617-107">Le applicazioni devono utilizzare la funzione [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="a2617-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="a2617-108">La funzione **RasAdminServerGetInfo** ottiene la configurazione del server di un server RAS.</span><span class="sxs-lookup"><span data-stu-id="a2617-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2617-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2617-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="a2617-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2617-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2617-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2617-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2617-112">Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del server RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a2617-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="a2617-113">Se questo parametro è **null**, la funzione restituisce informazioni sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="a2617-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="a2617-114">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="a2617-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="a2617-115">*pRasServer0* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a2617-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2617-116">Puntatore alla struttura [**del \_ server RAS \_ 0**](ras-server-0-str.md) che riceve il numero di porte configurate nel server, il numero di porte attualmente in uso e il numero di versione del server.</span><span class="sxs-lookup"><span data-stu-id="a2617-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2617-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2617-117">Return value</span></span>

<span data-ttu-id="a2617-118">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a2617-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a2617-119">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a2617-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="a2617-120">I codici di errore possibili includono quelli restituiti da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per la funzione [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="a2617-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="a2617-121">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="a2617-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2617-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2617-122">Remarks</span></span>

<span data-ttu-id="a2617-123">Per enumerare tutti i server RAS in un dominio, chiamare la funzione [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) e specificare SV \_ digitare \_ dialin per il parametro *ServerType* .</span><span class="sxs-lookup"><span data-stu-id="a2617-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2617-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2617-124">Requirements</span></span>



| <span data-ttu-id="a2617-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2617-125">Requirement</span></span> | <span data-ttu-id="a2617-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a2617-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2617-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a2617-127">End of client support</span></span><br/> | <span data-ttu-id="a2617-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2617-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a2617-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a2617-129">End of server support</span></span><br/> | <span data-ttu-id="a2617-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2617-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a2617-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2617-131">Header</span></span><br/>                | <dl> <span data-ttu-id="a2617-132"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2617-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2617-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2617-133">Library</span></span><br/>               | <dl> <span data-ttu-id="a2617-134"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2617-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2617-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a2617-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a2617-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2617-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2617-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2617-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2617-138">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="a2617-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a2617-139">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="a2617-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="a2617-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="a2617-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="a2617-141">**\_Server RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="a2617-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

