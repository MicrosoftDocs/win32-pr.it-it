---
title: Funzione RasAdminGetUserAccountServer (rassapi. h)
description: La funzione RasAdminGetUserAccountServer Recupera il nome del server con il database degli account utente. Usare il nome del server restituito nelle funzioni RasAdminUserGetInfo e RasAdminUserSetInfo per ottenere o impostare le informazioni relative a un utente specificato.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RAS funzione RasAdminGetUserAccountServer
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327903"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="711fb-105">RasAdminGetUserAccountServer (funzione)</span><span class="sxs-lookup"><span data-stu-id="711fb-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="711fb-106">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="711fb-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="711fb-107">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="711fb-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="711fb-108">Le applicazioni devono utilizzare la funzione [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]</span><span class="sxs-lookup"><span data-stu-id="711fb-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="711fb-109">La funzione **RasAdminGetUserAccountServer** Recupera il nome del server con il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="711fb-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="711fb-110">Usare il nome del server restituito nelle funzioni [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) per ottenere o impostare le informazioni relative a un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="711fb-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="711fb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="711fb-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="711fb-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="711fb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711fb-113">*lpszDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711fb-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711fb-114">Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del dominio a cui appartiene il server RAS.</span><span class="sxs-lookup"><span data-stu-id="711fb-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="711fb-115">Questo parametro è **null** per le applicazioni di amministrazione RAS in esecuzione su workstation o server che non sono membri di un dominio.</span><span class="sxs-lookup"><span data-stu-id="711fb-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="711fb-116">Se questo parametro è **null**, il parametro *lpszServer* deve essere diverso da **null**.</span><span class="sxs-lookup"><span data-stu-id="711fb-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="711fb-117">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="711fb-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711fb-118">Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del server RAS.</span><span class="sxs-lookup"><span data-stu-id="711fb-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="711fb-119">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="711fb-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="711fb-120">Questo parametro può essere **null** se il parametro *LpszDomain* non è **null**.</span><span class="sxs-lookup"><span data-stu-id="711fb-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="711fb-121">*lpszUserAccountServer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="711fb-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711fb-122">Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che specifica il nome di un controller di dominio con il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="711fb-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="711fb-123">Il buffer deve essere sufficientemente grande da contenere il nome del server (UNCLEn + 1).</span><span class="sxs-lookup"><span data-stu-id="711fb-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="711fb-124">La funzione prefissa il nome del server restituito con i \\ \\ caratteri "" iniziali, nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="711fb-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711fb-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="711fb-125">Return value</span></span>

<span data-ttu-id="711fb-126">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="711fb-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="711fb-127">Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="711fb-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="711fb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="711fb-128">Value</span></span>                                                                                                    | <span data-ttu-id="711fb-129">Significato</span><span class="sxs-lookup"><span data-stu-id="711fb-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="711fb-130"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="711fb-131">Sia *lpszDomain* che *lpszServer* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="711fb-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="711fb-132">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="711fb-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="711fb-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="711fb-133">Remarks</span></span>

<span data-ttu-id="711fb-134">La funzione **RasAdminGetUserAccountServer** ottiene il nome del server con il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="711fb-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="711fb-135">Questa funzione richiede il nome del server RAS o il nome del dominio in cui risiede il server RAS.</span><span class="sxs-lookup"><span data-stu-id="711fb-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="711fb-136">Il parametro *lpszDomain* deve specificare un nome di dominio valido.</span><span class="sxs-lookup"><span data-stu-id="711fb-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="711fb-137">Questo parametro è **null** per le applicazioni di amministrazione RAS in esecuzione su server che non sono membri di un dominio (ad esempio, il server si trova nel proprio gruppo di lavoro).</span><span class="sxs-lookup"><span data-stu-id="711fb-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="711fb-138">In questo caso, il parametro *lpszServer* deve specificare il nome del server.</span><span class="sxs-lookup"><span data-stu-id="711fb-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="711fb-139">Per ottenere il nome del server, chiamare la funzione [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) .</span><span class="sxs-lookup"><span data-stu-id="711fb-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="711fb-140">Assicurarsi di anteporre al nome del server i caratteri " \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="711fb-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="711fb-141">Se il nome del server specificato da *lpszServer* è un server autonomo (ovvero, il server o la workstation non è un membro di un dominio), il nome del server stesso viene restituito nel buffer *lpszUserAccountServer* .</span><span class="sxs-lookup"><span data-stu-id="711fb-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="711fb-142">Utilizzare quindi il nome del server di account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti nel database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="711fb-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="711fb-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="711fb-143">Requirements</span></span>



| <span data-ttu-id="711fb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="711fb-144">Requirement</span></span> | <span data-ttu-id="711fb-145">Valore</span><span class="sxs-lookup"><span data-stu-id="711fb-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="711fb-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="711fb-146">End of client support</span></span><br/> | <span data-ttu-id="711fb-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="711fb-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="711fb-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="711fb-148">End of server support</span></span><br/> | <span data-ttu-id="711fb-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="711fb-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="711fb-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="711fb-150">Header</span></span><br/>                | <dl> <span data-ttu-id="711fb-151"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="711fb-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="711fb-152">Library</span></span><br/>               | <dl> <span data-ttu-id="711fb-153"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="711fb-154">DLL</span><span class="sxs-lookup"><span data-stu-id="711fb-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="711fb-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711fb-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711fb-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="711fb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711fb-157">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="711fb-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="711fb-158">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="711fb-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="711fb-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="711fb-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="711fb-160">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="711fb-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="711fb-161">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="711fb-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

