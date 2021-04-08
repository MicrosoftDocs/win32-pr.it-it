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
# <a name="wzcenuminterfaces-function"></a>WZCEnumInterfaces (funzione)

\[**WZCEnumInterfaces** non è più supportato a partire da Windows Vista e windows Server 2008. Usare invece la funzione [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) . Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

La funzione **WZCEnumInterfaces** enumera tutte le interfacce LAN wireless gestite dal servizio di configurazione zero wireless.

## <a name="syntax"></a>Sintassi


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrvAddr* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione. Se questo parametro è **null**, il servizio di configurazione zero senza fili viene enumerato nel computer locale.

Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*pIntfs* \[ out\]
</dt> <dd>

Puntatore a una struttura [**della \_ \_ tabella della chiave INTFS**](intfs-key-table.md) che contiene una tabella di informazioni chiave per tutte le interfacce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.



| Codice restituito                                                                                               | Descrizione                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE nell' \_ Arena \_**</dt> </dl>      | I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente. Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.<br/> |
| <dl> <dt>**RPC \_ \_ sconosciuto \_ se**</dt> </dl>        | L'interfaccia è sconosciuta.<br/> Questo errore viene restituito se il servizio di configurazione zero wireless non è stato avviato.<br/>                             |
| <dl> <dt>**\_puntatore di \_ \_ riferimento null RPC X \_**</dt> </dl> | Un puntatore di riferimento null è stato passato allo stub.<br/> Questo errore viene restituito se il parametro *pIntfs* è **null**.<br/>                          |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl> | Memoria insufficiente per elaborare la richiesta e allocare memoria per i risultati della query.<br/>                                                  |
| <dl> <dt>**\_stato RPC**</dt> </dl>                | Codici di errore diversi.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Il membro **dwNumIntfs** della struttura [**della \_ \_ tabella della chiave INTFS**](intfs-key-table.md) a cui punta *pIntf* deve essere impostato su 0 prima di chiamare la funzione **WZCEnumInterfaces** . Inoltre, il membro **pIntfs** deve essere impostato su **null**.

Per le chiamate successive ad altre funzioni di configurazione di zero wireless, un'applicazione deve identificare l'interfaccia su cui sta operando fornendo le informazioni chiave rilevanti restituite dalla funzione **WZCEnumInterfaces** .

Se **WZCEnumInterfaces** restituisce Error \_ Success, il chiamante deve chiamare [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie.

> [!Note]  
> Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono enumerate le interfacce LAN wireless nel computer locale gestito dal servizio Wireless Zero Configuration e viene stampato il valore per GUID di interfaccia per ogni interfaccia.

> [!Note]  
> Questo esempio avrà esito negativo in Windows Vista e versioni successive.

 


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                         |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tabella della chiave INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**\_voce della chiave INTF \_**](intf-key-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
