---
title: Funzione RasAdminUserSetInfo (rassapi. h)
description: La funzione RasAdminUserSetInfo imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RAS funzione RasAdminUserSetInfo
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328059"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="b8ecf-104">RasAdminUserSetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8ecf-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="b8ecf-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b8ecf-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b8ecf-107">Le applicazioni devono utilizzare la funzione [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="b8ecf-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="b8ecf-108">La funzione **RasAdminUserSetInfo** imposta le autorizzazioni RAS e il numero di telefono di chiamata per un utente specificato.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ecf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8ecf-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="b8ecf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8ecf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ecf-111">*lpszUserAccountServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8ecf-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ecf-112">Puntatore a una stringa Unicode con terminazione null che specifica il nome del controller di dominio primario o di backup con il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="b8ecf-113">Utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="b8ecf-114">*lpszUser* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8ecf-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ecf-115">Puntatore a una stringa Unicode con terminazione null che specifica il nome dell'utente per il quale devono essere impostate le informazioni RAS.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b8ecf-116">*pRasUser0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8ecf-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ecf-117">Puntatore alla struttura [**\_ dell'utente RAS \_ 0**](ras-user-0-str.md) che specifica i nuovi dati RAS per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ecf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8ecf-118">Return value</span></span>

<span data-ttu-id="b8ecf-119">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b8ecf-120">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="b8ecf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8ecf-121">Value</span></span>                                                                                                           | <span data-ttu-id="b8ecf-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8ecf-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8ecf-123"><dt>**ERRORE \_ dati non validi \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="b8ecf-124">Il buffer *pRasUser0* contiene dati non validi.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b8ecf-125"><dt>**ERRORE \_ \_ numero di callback non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="b8ecf-126">Il numero di callback specificato nel buffer *pRasUser0* contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="b8ecf-127"><dt>**Nerr \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="b8ecf-128">Memoria insufficiente per eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="b8ecf-129">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b8ecf-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ecf-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8ecf-130">Remarks</span></span>

<span data-ttu-id="b8ecf-131">Quando si impostano le autorizzazioni RAS per un utente, è necessario che il membro **bfPrivilege** della struttura [**RAS \_ User \_ 0**](ras-user-0-str.md) specifichi almeno uno dei flag di chiamata.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="b8ecf-132">Ad esempio, per impostare i privilegi di un utente per consentire i privilegi di connessione remota senza privilegi di callback, impostare **bfPrivilege** su RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback.</span><span class="sxs-lookup"><span data-stu-id="b8ecf-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ecf-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8ecf-133">Requirements</span></span>



| <span data-ttu-id="b8ecf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ecf-134">Requirement</span></span> | <span data-ttu-id="b8ecf-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b8ecf-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ecf-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b8ecf-136">End of client support</span></span><br/> | <span data-ttu-id="b8ecf-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b8ecf-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b8ecf-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b8ecf-138">End of server support</span></span><br/> | <span data-ttu-id="b8ecf-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8ecf-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b8ecf-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8ecf-140">Header</span></span><br/>                | <dl> <span data-ttu-id="b8ecf-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8ecf-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8ecf-142">Library</span></span><br/>               | <dl> <span data-ttu-id="b8ecf-143"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8ecf-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b8ecf-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b8ecf-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecf-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ecf-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8ecf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ecf-147">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b8ecf-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b8ecf-148">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="b8ecf-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b8ecf-149">**\_Utente RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="b8ecf-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="b8ecf-150">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="b8ecf-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="b8ecf-151">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b8ecf-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

