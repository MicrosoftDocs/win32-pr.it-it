---
title: Funzione RasAdminUserGetInfo (rassapi. h)
description: La funzione RasAdminUserGetInfo ottiene le informazioni relative al numero di telefono di callback e alle autorizzazioni RAS per un utente specificato.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RAS funzione RasAdminUserGetInfo
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327900"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="00a6e-104">RasAdminUserGetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="00a6e-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="00a6e-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="00a6e-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="00a6e-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00a6e-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="00a6e-107">Le applicazioni devono utilizzare la funzione [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="00a6e-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="00a6e-108">La funzione **RasAdminUserGetInfo** ottiene le informazioni relative al numero di telefono di callback e alle autorizzazioni RAS per un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="00a6e-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a6e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a6e-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="00a6e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="00a6e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a6e-111">*lpszUserAccountServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a6e-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a6e-112">Puntatore a una stringa Unicode con terminazione null che specifica il nome del controller di dominio primario o di backup con il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="00a6e-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="00a6e-113">Utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.</span><span class="sxs-lookup"><span data-stu-id="00a6e-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="00a6e-114">*lpszUser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a6e-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a6e-115">Puntatore a una stringa Unicode con terminazione null che specifica il nome dell'utente per il quale ottenere le informazioni RAS.</span><span class="sxs-lookup"><span data-stu-id="00a6e-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="00a6e-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="00a6e-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="00a6e-117">Puntatore alla struttura [**dell' \_ utente RAS \_ 0**](ras-user-0-str.md) che riceve i dati RAS per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="00a6e-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a6e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00a6e-118">Return value</span></span>

<span data-ttu-id="00a6e-119">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="00a6e-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="00a6e-120">Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="00a6e-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="00a6e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="00a6e-121">Value</span></span>                                                                                            | <span data-ttu-id="00a6e-122">Significato</span><span class="sxs-lookup"><span data-stu-id="00a6e-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="00a6e-123"><dt>**\_BUFTOOSMALL Nerr**</dt></span><span class="sxs-lookup"><span data-stu-id="00a6e-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="00a6e-124">Memoria insufficiente per eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="00a6e-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="00a6e-125">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="00a6e-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a6e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a6e-126">Requirements</span></span>



| <span data-ttu-id="00a6e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a6e-127">Requirement</span></span> | <span data-ttu-id="00a6e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="00a6e-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00a6e-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="00a6e-129">End of client support</span></span><br/> | <span data-ttu-id="00a6e-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00a6e-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="00a6e-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="00a6e-131">End of server support</span></span><br/> | <span data-ttu-id="00a6e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00a6e-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="00a6e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00a6e-133">Header</span></span><br/>                | <dl> <span data-ttu-id="00a6e-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a6e-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="00a6e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="00a6e-135">Library</span></span><br/>               | <dl> <span data-ttu-id="00a6e-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00a6e-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="00a6e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="00a6e-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="00a6e-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a6e-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a6e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a6e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a6e-140">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="00a6e-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="00a6e-141">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="00a6e-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="00a6e-142">**\_Utente RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="00a6e-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="00a6e-143">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="00a6e-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="00a6e-144">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="00a6e-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

