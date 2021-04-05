---
description: Fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio di configurazione wireless zero.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Funzione WZCQueryInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884546"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="eab14-103">WZCQueryInterface (funzione)</span><span class="sxs-lookup"><span data-stu-id="eab14-103">WZCQueryInterface function</span></span>

<span data-ttu-id="eab14-104">\[**WZCQueryInterface** non è più supportato a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="eab14-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="eab14-105">Usare invece la funzione [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="eab14-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="eab14-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="eab14-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="eab14-107">\]</span><span class="sxs-lookup"><span data-stu-id="eab14-107">\]</span></span>

<span data-ttu-id="eab14-108">La funzione **WZCQueryInterface** fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio di configurazione wireless zero.</span><span class="sxs-lookup"><span data-stu-id="eab14-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="eab14-109">Fornisce informazioni dettagliate per una determinata interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab14-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eab14-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="eab14-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="eab14-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab14-112">*pSrvAddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eab14-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab14-113">Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="eab14-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="eab14-114">Se questo parametro è **null**, viene eseguita una query sul servizio di configurazione zero wireless nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="eab14-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="eab14-115">Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.</span><span class="sxs-lookup"><span data-stu-id="eab14-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="eab14-116">*dwInFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eab14-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab14-117">Campi su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="eab14-117">The fields to be queried.</span></span> <span data-ttu-id="eab14-118">Si tratta di una maschera di maschera che può contenere qualsiasi combinazione dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="eab14-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="eab14-119">Valore</span><span class="sxs-lookup"><span data-stu-id="eab14-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="eab14-120">Significato</span><span class="sxs-lookup"><span data-stu-id="eab14-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="eab14-121"><dt>**INTF \_**</dt> <dt>0x00000010</dt> DYNFLAGS</span><span class="sxs-lookup"><span data-stu-id="eab14-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="eab14-122">Restituisce il valore per il membro **dwDynFlags** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="eab14-123"><dt>**INTF \_ 0x00010000 DESCr**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eab14-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="eab14-124">Restituisce il valore per il membro **wszDescr** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="eab14-125"><dt>**INTF \_**</dt> <dt>0x00020000</dt> NDISMEDIA</span><span class="sxs-lookup"><span data-stu-id="eab14-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="eab14-126">Restituisce i valori per i membri **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** nella struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="eab14-127"><dt>**INTF \_**</dt> <dt>0x00040000</dt> PREFLIST</span><span class="sxs-lookup"><span data-stu-id="eab14-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="eab14-128">Restituisce l'elenco preferito di reti nel membro **rdStSSIDList** della struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="eab14-129"><dt>**INTF \_ FUNZIONALITÀ**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="eab14-130">Restituisce i valori per i membri **dwCapabilities** e **rdNicCapabilities** nella struttura di [**\_ voci INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="eab14-131"><dt>**INTF \_**</dt> <dt>0x00200000</dt> INFRAMODE</span><span class="sxs-lookup"><span data-stu-id="eab14-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="eab14-132">Restituisce il valore per il membro **nInfraMode** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="eab14-133">Il membro **nInfraMode** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="eab14-134"><dt>**INTF \_**</dt> <dt>0x00400000</dt> AUTHMODE</span><span class="sxs-lookup"><span data-stu-id="eab14-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="eab14-135">Restituisce il valore per il membro **nAuthMode** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="eab14-136">Il membro **nAuthMode** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="eab14-137"><dt>**INTF \_**</dt> <dt>0x00800000</dt> WEPSTATUS</span><span class="sxs-lookup"><span data-stu-id="eab14-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="eab14-138">Restituisce il valore per il membro **nWepStatus** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="eab14-139">Il membro **nWepStatus** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="eab14-140"><dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="eab14-141">Restituisce il valore per il membro **rdSSID** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="eab14-142">Il membro **rdSSID** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="eab14-143"><dt>**INTF \_**</dt> <dt>0x02000000</dt> BSSID</span><span class="sxs-lookup"><span data-stu-id="eab14-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="eab14-144">Restituisce il valore per il membro **rdBSSID** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="eab14-145">Il membro **rdBSSID** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="eab14-146"><dt>**INTF \_**</dt> <dt>0x04000000</dt> BSSIDLIST</span><span class="sxs-lookup"><span data-stu-id="eab14-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="eab14-147">Restituisce l'elenco visibile di reti nel membro **rdBSSIDList** della struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="eab14-148">Il membro **rdBSSIDList** è valido solo in alcuni Stati del contesto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eab14-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eab14-149">*pIntf* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="eab14-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eab14-150">In input, puntatore alla chiave dell'interfaccia su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="eab14-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="eab14-151">Nell'output, puntatore ai dati dell'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="eab14-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="eab14-152">Questo parametro è un puntatore a una struttura di [**\_ voce INTF**](intf-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="eab14-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eab14-153">*pdwOutFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eab14-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eab14-154">Set di campi recuperato correttamente.</span><span class="sxs-lookup"><span data-stu-id="eab14-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab14-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eab14-155">Return value</span></span>

<span data-ttu-id="eab14-156">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="eab14-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="eab14-157">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="eab14-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="eab14-158">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="eab14-158">Return code</span></span>                                                                                               | <span data-ttu-id="eab14-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eab14-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eab14-160"><dt>**ERRORE nell' \_ Arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="eab14-161">I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="eab14-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="eab14-162">Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.</span><span class="sxs-lookup"><span data-stu-id="eab14-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="eab14-163"><dt>**FILE di errore \_ \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="eab14-164">Non è possibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="eab14-164">The system cannot find the file specified.</span></span> <span data-ttu-id="eab14-165">Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *PINTF* non corrisponde ad alcuna interfaccia LAN wireless nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="eab14-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="eab14-166"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="eab14-167">Un parametro non è corretto.</span><span class="sxs-lookup"><span data-stu-id="eab14-167">A parameter is incorrect.</span></span> <span data-ttu-id="eab14-168">Questo errore viene restituito se il parametro *pIntf* è **null**.</span><span class="sxs-lookup"><span data-stu-id="eab14-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="eab14-169">Questo errore viene restituito se il membro **wszGuid** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* è **null**.</span><span class="sxs-lookup"><span data-stu-id="eab14-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="eab14-170"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="eab14-171">Memoria insufficiente per elaborare la richiesta e allocare memoria per i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="eab14-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="eab14-172"><dt>**\_stato RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="eab14-173">Codici di errore diversi.</span><span class="sxs-lookup"><span data-stu-id="eab14-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="eab14-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="eab14-174">Remarks</span></span>

<span data-ttu-id="eab14-175">Il membro **wszGuid** della struttura [**di \_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="eab14-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="eab14-176">È possibile recuperare un elenco di interfacce LAN wireless chiamando la funzione [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="eab14-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="eab14-177">I membri seguenti della struttura [**di \_ voci INTF**](intf-entry.md) a cui punta *pIntf* devono essere impostati su 0 prima di una chiamata alla funzione **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** e **rdCtrlData**.</span><span class="sxs-lookup"><span data-stu-id="eab14-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="eab14-178">Il servizio di configurazione zero senza fili non automotically lo stato di aggiornamento dei supporti, anche quando vengono ricevuti gli eventi di supporto connessi e disconnessi.</span><span class="sxs-lookup"><span data-stu-id="eab14-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="eab14-179">Un'applicazione deve forzare un aggiornamento dello stato multimediale chiamando la funzione [**WZCRefreshInterface**](wzcrefreshinterface.md) prima di chiamare la funzione **WZCQueryInterface** se è necessario richiedere lo stato del supporto NDIS (il \_ bit NDISMEDIA di INTF verrà impostato nel parametro *dwInFlags* ).</span><span class="sxs-lookup"><span data-stu-id="eab14-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="eab14-180">Quando il parametro *dwInFlags* contiene **INTF \_ BSSIDLIST**, la funzione **WZCQueryInterface** non imposta la *dwOutFlags* con **INTF \_ BSSIDLIST** se l'elenco di reti visibile è vuoto.</span><span class="sxs-lookup"><span data-stu-id="eab14-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="eab14-181">Quando il parametro *dwInFlags* contiene **INTF \_ SSID**, la funzione **WZCQueryInterface** non imposta *dwOutFlags* con **INTF \_ SSID** se non è disponibile alcun SSID.</span><span class="sxs-lookup"><span data-stu-id="eab14-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="eab14-182">Se la funzione **WZCQueryInterface** restituisce l'errore \_ Success, il chiamante deve chiamare la funzione [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) con il parametro *pIntf* per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="eab14-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="eab14-183">In questo modo vengono rilasciati i buffer usati dai membri **rdSSID**, **rdBSSID**, **rdBSSIDList**, **RdStSSIDList** e **rdCtrlData** della struttura di [**\_ voci INTF**](intf-entry.md) a cui punta il parametro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="eab14-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="eab14-184">Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="eab14-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eab14-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eab14-185">Requirements</span></span>



| <span data-ttu-id="eab14-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab14-186">Requirement</span></span> | <span data-ttu-id="eab14-187">Valore</span><span class="sxs-lookup"><span data-stu-id="eab14-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eab14-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eab14-188">Minimum supported client</span></span><br/> | <span data-ttu-id="eab14-189">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eab14-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eab14-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eab14-190">Minimum supported server</span></span><br/> | <span data-ttu-id="eab14-191">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eab14-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eab14-192">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="eab14-192">End of client support</span></span><br/>    | <span data-ttu-id="eab14-193">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="eab14-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="eab14-194">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="eab14-194">End of server support</span></span><br/>    | <span data-ttu-id="eab14-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eab14-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="eab14-196">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eab14-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab14-197"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="eab14-198">Libreria</span><span class="sxs-lookup"><span data-stu-id="eab14-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="eab14-199"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="eab14-200">DLL</span><span class="sxs-lookup"><span data-stu-id="eab14-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab14-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab14-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab14-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eab14-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab14-203">**\_voce INTF**</span><span class="sxs-lookup"><span data-stu-id="eab14-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="eab14-204">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="eab14-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="eab14-205">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="eab14-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="eab14-206">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="eab14-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
