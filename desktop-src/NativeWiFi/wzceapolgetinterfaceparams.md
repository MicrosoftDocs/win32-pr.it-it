---
description: Ottiene i parametri di configurazione avvio EAPOL per l'interfaccia LAN wireless specificata.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Funzione WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317105"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="35bd7-103">WZCEapolGetInterfaceParams (funzione)</span><span class="sxs-lookup"><span data-stu-id="35bd7-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="35bd7-104">\[**WZCEapolGetInterfaceParams** non è più supportato a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="35bd7-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="35bd7-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="35bd7-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="35bd7-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="35bd7-107">La funzione **WZCEapolGetInterfaceParams** ottiene i parametri di configurazione di avvio EAPOL per l'interfaccia LAN wireless specificata.</span><span class="sxs-lookup"><span data-stu-id="35bd7-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="35bd7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35bd7-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="35bd7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35bd7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35bd7-110">*pSrvAddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35bd7-111">Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="35bd7-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="35bd7-112">Se questo parametro è **null**, il servizio di configurazione zero senza fili viene chiamato sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="35bd7-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="35bd7-113">Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.</span><span class="sxs-lookup"><span data-stu-id="35bd7-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="35bd7-114">*pwszGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35bd7-115">GUID dell'interfaccia per cui recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="35bd7-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="35bd7-116">*dwSizeOfSSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35bd7-117">Dimensioni dell'identificatore di rete per cui devono essere recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="35bd7-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="35bd7-118">*pbSSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35bd7-119">Puntatore all'identificatore di rete per il quale devono essere recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="35bd7-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="35bd7-120">*pIntfParams* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35bd7-121">Puntatore a una struttura [**avvio EAPOL \_ INTF \_ params**](eapol-intf-params.md) che contiene i parametri dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="35bd7-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35bd7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35bd7-122">Return value</span></span>

<span data-ttu-id="35bd7-123">Restituisce \_ l'errore se l'operazione viene completata correttamente; in caso contrario, restituisce uno dei codici di errore di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="35bd7-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="35bd7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="35bd7-124">Remarks</span></span>

<span data-ttu-id="35bd7-125">Se **WZCEapolGetInterfaceParams** restituisce Error \_ Success, il chiamante deve chiamare [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="35bd7-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="35bd7-126">Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="35bd7-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35bd7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35bd7-127">Requirements</span></span>



| <span data-ttu-id="35bd7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="35bd7-128">Requirement</span></span> | <span data-ttu-id="35bd7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="35bd7-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35bd7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35bd7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35bd7-131">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35bd7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35bd7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35bd7-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35bd7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35bd7-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="35bd7-134">End of client support</span></span><br/>    | <span data-ttu-id="35bd7-135">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="35bd7-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="35bd7-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="35bd7-136">End of server support</span></span><br/>    | <span data-ttu-id="35bd7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35bd7-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="35bd7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35bd7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="35bd7-139"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35bd7-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="35bd7-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="35bd7-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="35bd7-141"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35bd7-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="35bd7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="35bd7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35bd7-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35bd7-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35bd7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35bd7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35bd7-145">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="35bd7-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="35bd7-146">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="35bd7-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="35bd7-147">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="35bd7-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
