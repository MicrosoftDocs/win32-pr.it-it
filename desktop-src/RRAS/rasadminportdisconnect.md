---
title: Funzione RasAdminPortDisconnect (rassapi. h)
description: La funzione RasAdminPortDisconnect disconnette una porta attualmente in uso.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RAS funzione RasAdminPortDisconnect
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330767"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="c7403-104">RasAdminPortDisconnect (funzione)</span><span class="sxs-lookup"><span data-stu-id="c7403-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="c7403-105">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c7403-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c7403-106">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c7403-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c7403-107">Le applicazioni devono utilizzare la funzione [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]</span><span class="sxs-lookup"><span data-stu-id="c7403-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="c7403-108">La funzione **RasAdminPortDisconnect** disconnette una porta attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="c7403-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7403-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7403-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="c7403-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7403-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7403-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7403-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7403-112">Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c7403-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="c7403-113">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="c7403-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="c7403-114">*lpszPort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7403-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7403-115">Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta nel server.</span><span class="sxs-lookup"><span data-stu-id="c7403-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7403-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7403-116">Return value</span></span>

<span data-ttu-id="c7403-117">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c7403-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c7403-118">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici di errore.</span><span class="sxs-lookup"><span data-stu-id="c7403-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="c7403-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c7403-119">Value</span></span>                                                                                               | <span data-ttu-id="c7403-120">Significato</span><span class="sxs-lookup"><span data-stu-id="c7403-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c7403-121"><dt>**ERRORE \_ porta non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7403-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="c7403-122">La porta specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="c7403-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="c7403-123"><dt>**\_USERNOTFOUND Nerr**</dt></span><span class="sxs-lookup"><span data-stu-id="c7403-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="c7403-124">La porta non è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="c7403-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="c7403-125">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c7403-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7403-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7403-126">Requirements</span></span>



| <span data-ttu-id="c7403-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7403-127">Requirement</span></span> | <span data-ttu-id="c7403-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c7403-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7403-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c7403-129">End of client support</span></span><br/> | <span data-ttu-id="c7403-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7403-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c7403-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c7403-131">End of server support</span></span><br/> | <span data-ttu-id="c7403-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7403-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c7403-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7403-133">Header</span></span><br/>                | <dl> <span data-ttu-id="c7403-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7403-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7403-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7403-135">Library</span></span><br/>               | <dl> <span data-ttu-id="c7403-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7403-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7403-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7403-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c7403-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7403-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7403-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7403-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7403-140">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="c7403-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c7403-141">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="c7403-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

