---
title: Funzione RasAdminPortEnum (rassapi. h)
description: La funzione RasAdminPortEnum enumera tutte le porte nel server RAS specificato. Per ogni porta sul server, la funzione restituisce la struttura della \_ porta RAS \_ 0 che contiene le informazioni sulla porta.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RAS funzione RasAdminPortEnum
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327901"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="b3aa1-105">RasAdminPortEnum (funzione)</span><span class="sxs-lookup"><span data-stu-id="b3aa1-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="b3aa1-106">\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b3aa1-107">Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b3aa1-108">Le applicazioni devono utilizzare la funzione [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]</span><span class="sxs-lookup"><span data-stu-id="b3aa1-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="b3aa1-109">La funzione **RasAdminPortEnum** enumera tutte le porte nel server RAS specificato.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="b3aa1-110">Per ogni porta sul server, la funzione restituisce la struttura [**della \_ porta RAS \_ 0**](ras-port-0-str.md) che contiene le informazioni sulla porta.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3aa1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3aa1-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="b3aa1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3aa1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3aa1-113">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3aa1-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3aa1-114">Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="b3aa1-115">Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="b3aa1-116">*ppRasPort0* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3aa1-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3aa1-117">Puntatore a una variabile che riceve un puntatore a un buffer che contiene una matrice di strutture della [**\_ porta RAS \_ 0**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="b3aa1-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="b3aa1-118">Quando l'applicazione ha terminato con la memoria, liberarla chiamando la funzione [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b3aa1-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b3aa1-119">*pcEntriesRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b3aa1-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3aa1-120">Puntatore a una variabile a 16 bit che riceve il numero totale di strutture [**RAS della \_ porta \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) restituite nella matrice *ppRasPort0* .</span><span class="sxs-lookup"><span data-stu-id="b3aa1-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3aa1-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3aa1-121">Return value</span></span>

<span data-ttu-id="b3aa1-122">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b3aa1-123">Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="b3aa1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b3aa1-124">Value</span></span>                                                                                             | <span data-ttu-id="b3aa1-125">Significato</span><span class="sxs-lookup"><span data-stu-id="b3aa1-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3aa1-126"><dt>**\_ITEMNOTFOUND Nerr**</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa1-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="b3aa1-127">Non è stato possibile enumerare le porte.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-127">No ports could be enumerated.</span></span> <span data-ttu-id="b3aa1-128">Questo potrebbe essere dovuto al fatto che tutte le porte configurate nel server sono attualmente in uso per la connessione.</span><span class="sxs-lookup"><span data-stu-id="b3aa1-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="b3aa1-129">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b3aa1-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3aa1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3aa1-130">Requirements</span></span>



| <span data-ttu-id="b3aa1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3aa1-131">Requirement</span></span> | <span data-ttu-id="b3aa1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b3aa1-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3aa1-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b3aa1-133">End of client support</span></span><br/> | <span data-ttu-id="b3aa1-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b3aa1-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b3aa1-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b3aa1-135">End of server support</span></span><br/> | <span data-ttu-id="b3aa1-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3aa1-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b3aa1-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3aa1-137">Header</span></span><br/>                | <dl> <span data-ttu-id="b3aa1-138"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa1-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3aa1-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3aa1-139">Library</span></span><br/>               | <dl> <span data-ttu-id="b3aa1-140"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa1-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3aa1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b3aa1-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b3aa1-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa1-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3aa1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3aa1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3aa1-144">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b3aa1-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b3aa1-145">Funzioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="b3aa1-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b3aa1-146">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="b3aa1-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="b3aa1-147">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="b3aa1-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

