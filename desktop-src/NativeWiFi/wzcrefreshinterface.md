---
description: Aggiorna le informazioni sull'interfaccia per una specifica interfaccia LAN wireless.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Funzione WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348111"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="5c2c3-103">WZCRefreshInterface (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c2c3-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="5c2c3-104">\[**WZCRefreshInterface** non è supportato a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5c2c3-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="5c2c3-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="5c2c3-107">La funzione **WZCRefreshInterface** aggiorna le informazioni sull'interfaccia per una specifica interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c2c3-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5c2c3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c2c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2c3-110">*pSrvAddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c3-111">Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="5c2c3-112">Se questo parametro è **null**, il servizio di configurazione zero senza fili viene chiamato sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="5c2c3-113">Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="5c2c3-114">*dwInFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c3-115">Set di campi da aggiornare insieme a specifiche azioni di aggiornamento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="5c2c3-116">Si tratta di una maschera di maschera che può contenere qualsiasi combinazione dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="5c2c3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5c2c3-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="5c2c3-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5c2c3-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="5c2c3-119"><dt>**INTF \_ 0x00010000 DESCr**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="5c2c3-120">Aggiornare la descrizione dell'interfaccia per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="5c2c3-121">La descrizione dell'interfaccia aggiornata può essere recuperata chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ Descr** impostato nel parametro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="5c2c3-122">La descrizione dell'interfaccia viene restituita nel membro **wszDescr** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* restituito dalla funzione **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="5c2c3-123"><dt>**INTF \_**</dt> <dt>0x00020000</dt> NDISMEDIA</span><span class="sxs-lookup"><span data-stu-id="5c2c3-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="5c2c3-124">Aggiornare le informazioni sui supporti NDIS per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="5c2c3-125">Le informazioni sul supporto NDIS aggiornate possono essere recuperate chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ NDISMEDIA** impostato nel parametro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="5c2c3-126">Le informazioni sui supporti NDIS vengono restituite nei membri **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* restituito dalla funzione **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="5c2c3-127"><dt>**INTF \_ TUTTI \_ OID**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="5c2c3-128">Aggiornare tutti i OID NDIS per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="5c2c3-129">Questa opzione consente di aggiornare la maggior parte dei dati per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="5c2c3-130">Le informazioni aggiornate possono essere recuperate chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="5c2c3-131">*pIntf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c3-132">Puntatore a una struttura [**di \_ voci INTF**](intf-entry.md) che contiene la chiave dell'interfaccia da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="5c2c3-133">*pdwOutFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2c3-134">Set di campi che sono stati aggiornati correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2c3-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c2c3-135">Return value</span></span>

<span data-ttu-id="5c2c3-136">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5c2c3-137">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="5c2c3-138">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c2c3-138">Return code</span></span>                                                                                              | <span data-ttu-id="5c2c3-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c2c3-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c2c3-140"><dt>**ERRORE nell' \_ Arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="5c2c3-141">I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="5c2c3-142">Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="5c2c3-143"><dt>**FILE di errore \_ \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="5c2c3-144">Non è possibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-144">The system cannot find the file specified.</span></span> <span data-ttu-id="5c2c3-145">Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *PINTF* non corrisponde ad alcuna interfaccia LAN wireless nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="5c2c3-146"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="5c2c3-147">Un parametro non è corretto.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-147">A parameter is incorrect.</span></span> <span data-ttu-id="5c2c3-148">Questo errore viene restituito se il parametro *pIntf* è **null**.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="5c2c3-149">Questo errore viene restituito se il membro **wszGuid** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* è **null**.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="5c2c3-150"><dt>**\_stato RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="5c2c3-151">Codici di errore diversi.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5c2c3-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c2c3-152">Remarks</span></span>

<span data-ttu-id="5c2c3-153">Il membro **wszGuid** della struttura [**di \_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="5c2c3-154">È possibile recuperare un elenco di interfacce LAN wireless chiamando la funzione [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2c3-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="5c2c3-155">Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5c2c3-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c2c3-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c2c3-156">Requirements</span></span>



| <span data-ttu-id="5c2c3-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2c3-157">Requirement</span></span> | <span data-ttu-id="5c2c3-158">Valore</span><span class="sxs-lookup"><span data-stu-id="5c2c3-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2c3-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c2c3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2c3-160">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c2c3-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c2c3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2c3-162">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c2c3-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c2c3-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5c2c3-163">End of client support</span></span><br/>    | <span data-ttu-id="5c2c3-164">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="5c2c3-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="5c2c3-165">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5c2c3-165">End of server support</span></span><br/>    | <span data-ttu-id="5c2c3-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c2c3-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5c2c3-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c2c3-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2c3-168"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c2c3-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c2c3-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c2c3-170"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c2c3-171">DLL</span><span class="sxs-lookup"><span data-stu-id="5c2c3-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c2c3-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c2c3-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2c3-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c2c3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2c3-174">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="5c2c3-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="5c2c3-175">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="5c2c3-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="5c2c3-176">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="5c2c3-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="5c2c3-177">**\_voce INTF**</span><span class="sxs-lookup"><span data-stu-id="5c2c3-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




