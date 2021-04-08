---
description: Enumera tutte le interfacce LAN wireless gestite dal servizio di configurazione zero wireless.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Funzione WZCEnumInterfaces (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884545"
---
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="568cf-103">WZCEnumInterfaces (funzione)</span><span class="sxs-lookup"><span data-stu-id="568cf-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="568cf-104">\[**WZCEnumInterfaces** non è più supportato a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="568cf-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="568cf-105">Usare invece la funzione [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) .</span><span class="sxs-lookup"><span data-stu-id="568cf-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="568cf-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="568cf-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="568cf-107">La funzione **WZCEnumInterfaces** enumera tutte le interfacce LAN wireless gestite dal servizio di configurazione zero wireless.</span><span class="sxs-lookup"><span data-stu-id="568cf-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="568cf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="568cf-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="568cf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="568cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568cf-110">*pSrvAddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="568cf-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="568cf-111">Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione.</span><span class="sxs-lookup"><span data-stu-id="568cf-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="568cf-112">Se questo parametro è **null**, il servizio di configurazione zero senza fili viene enumerato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="568cf-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="568cf-113">Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.</span><span class="sxs-lookup"><span data-stu-id="568cf-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="568cf-114">*pIntfs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="568cf-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="568cf-115">Puntatore a una struttura [**della \_ \_ tabella della chiave INTFS**](intfs-key-table.md) che contiene una tabella di informazioni chiave per tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="568cf-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568cf-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="568cf-116">Return value</span></span>

<span data-ttu-id="568cf-117">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="568cf-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="568cf-118">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="568cf-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="568cf-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="568cf-119">Return code</span></span>                                                                                               | <span data-ttu-id="568cf-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="568cf-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="568cf-121"><dt>**ERRORE nell' \_ Arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="568cf-122">I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="568cf-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="568cf-123">Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.</span><span class="sxs-lookup"><span data-stu-id="568cf-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="568cf-124"><dt>**RPC \_ \_ sconosciuto \_ se**</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="568cf-125">L'interfaccia è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="568cf-125">The interface is unknown.</span></span><br/> <span data-ttu-id="568cf-126">Questo errore viene restituito se il servizio di configurazione zero wireless non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="568cf-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="568cf-127"><dt>**\_puntatore di \_ \_ riferimento null RPC X \_**</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="568cf-128">Un puntatore di riferimento null è stato passato allo stub.</span><span class="sxs-lookup"><span data-stu-id="568cf-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="568cf-129">Questo errore viene restituito se il parametro *pIntfs* è **null**.</span><span class="sxs-lookup"><span data-stu-id="568cf-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="568cf-130"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="568cf-131">Memoria insufficiente per elaborare la richiesta e allocare memoria per i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="568cf-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="568cf-132"><dt>**\_stato RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="568cf-133">Codici di errore diversi.</span><span class="sxs-lookup"><span data-stu-id="568cf-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="568cf-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="568cf-134">Remarks</span></span>

<span data-ttu-id="568cf-135">Il membro **dwNumIntfs** della struttura [**della \_ \_ tabella della chiave INTFS**](intfs-key-table.md) a cui punta *pIntf* deve essere impostato su 0 prima di chiamare la funzione **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="568cf-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="568cf-136">Inoltre, il membro **pIntfs** deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="568cf-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="568cf-137">Per le chiamate successive ad altre funzioni di configurazione di zero wireless, un'applicazione deve identificare l'interfaccia su cui sta operando fornendo le informazioni chiave rilevanti restituite dalla funzione **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="568cf-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="568cf-138">Se **WZCEnumInterfaces** restituisce Error \_ Success, il chiamante deve chiamare [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="568cf-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="568cf-139">Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="568cf-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="568cf-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="568cf-140">Examples</span></span>

<span data-ttu-id="568cf-141">Nell'esempio seguente vengono enumerate le interfacce LAN wireless nel computer locale gestito dal servizio Wireless Zero Configuration e viene stampato il valore per GUID di interfaccia per ogni interfaccia.</span><span class="sxs-lookup"><span data-stu-id="568cf-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="568cf-142">Questo esempio avrà esito negativo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="568cf-142">This example will fail on Windows Vista and later .</span></span>

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="568cf-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="568cf-143">Requirements</span></span>



| <span data-ttu-id="568cf-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="568cf-144">Requirement</span></span> | <span data-ttu-id="568cf-145">Valore</span><span class="sxs-lookup"><span data-stu-id="568cf-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="568cf-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="568cf-146">Minimum supported client</span></span><br/> | <span data-ttu-id="568cf-147">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="568cf-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="568cf-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="568cf-148">Minimum supported server</span></span><br/> | <span data-ttu-id="568cf-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="568cf-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="568cf-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="568cf-150">End of client support</span></span><br/>    | <span data-ttu-id="568cf-151">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="568cf-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="568cf-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="568cf-152">End of server support</span></span><br/>    | <span data-ttu-id="568cf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="568cf-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="568cf-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="568cf-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="568cf-155"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="568cf-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="568cf-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="568cf-157"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="568cf-158">DLL</span><span class="sxs-lookup"><span data-stu-id="568cf-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="568cf-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="568cf-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="568cf-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="568cf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="568cf-161">**\_tabella della chiave INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="568cf-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="568cf-162">**\_voce della chiave INTF \_**</span><span class="sxs-lookup"><span data-stu-id="568cf-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="568cf-163">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="568cf-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="568cf-164">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="568cf-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="568cf-165">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="568cf-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
