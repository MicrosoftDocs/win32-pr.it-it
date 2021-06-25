---
title: Parole chiave dinamiche del firewall
description: Usare le API delle parole chiave dinamiche del firewall per gestire gli indirizzi delle parole chiave dinamiche Microsoft Defender Firewall.
keywords:
- Parole chiave dinamiche del firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: 15e35f26b72ed8d685e8302f6222836507e5c6a3
ms.sourcegitcommit: ae8c320a757558262167a4f4e385235b8d89035c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112765535"
---
# <a name="firewall-dynamic-keywords"></a>Parole chiave dinamiche del firewall

Usare le API delle parole chiave dinamiche del firewall per gestire *gli indirizzi delle parole chiave* dinamiche in [Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security). Un indirizzo di parola chiave dinamico viene usato per creare un set di indirizzi IP a cui possono fare riferimento una o più regole del firewall. Gli indirizzi delle parole chiave dinamiche supportano sia IPv4 che IPv6.

> [!NOTE]
> Per il contenuto di riferimento sulle API per le API introdotte in questo argomento, vedere Informazioni di riferimento [sulle parole chiave dinamiche del firewall.](firewall-dynamic-keywords-reference.md)

## <a name="operations-on-dynamic-keyword-addresses"></a>Operazioni sugli indirizzi delle parole chiave dinamiche

Con le API delle parole chiave dinamiche del firewall, è possibile eseguire le operazioni seguenti.

* Aggiungere indirizzi di parole chiave dinamiche
* Eliminare gli indirizzi delle parole chiave dinamiche
* Enumerare gli indirizzi delle parole chiave dinamiche in base all'ID o al tipo
* Aggiornare gli indirizzi delle parole chiave dinamiche
* Sottoscrivere e gestire le notifiche dinamiche di modifica degli indirizzi delle parole chiave

Sono disponibili esempi di codice per tutte queste operazioni più avanti in questo argomento.

Dopo aver aggiunto un indirizzo di parola chiave dinamico, l'indirizzo persiste tra i riavvii. Al termine dell'operazione, è necessario eliminare un indirizzo di parola chiave dinamico.

Esistono due classi di indirizzi di parole chiave dinamici, come descritto nelle due sezioni successive.

## <a name="autoresolve-dynamic-keyword-addresses"></a>Risolvere automaticamente gli indirizzi delle parole chiave dinamiche

Il primo tipo è *AutoResolve,* dove il campo della parola chiave rappresenta un nome risolvibile e gli indirizzi IP non sono definiti al momento della creazione. 

Questi oggetti hanno lo scopo di risolvere automaticamente gli indirizzi IP. Cio' non tramite un amministratore in fase di creazione dell'oggetto; né tramite il sistema operativo stesso. Un componente esterno al servizio firewall deve eseguire la risoluzione degli indirizzi IP per questi oggetti e aggiornarli in modo appropriato. L'implementazione di tale componente non rientra nell'ambito di questo contenuto.

Un indirizzo di parola chiave dinamico viene indicato come *AutoResolve* impostando il **flag** FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE nell'oggetto quando si chiama la [**funzione FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) Il *campo della* parola chiave deve essere usato per rappresentare il valore risolto, ovvero un nome di dominio completo &mdash; (FQDN) o un nome host. Il *campo addresses* deve inizialmente essere NULL per questi oggetti. Gli indirizzi IP di questi oggetti non saranno persistenti tra i cicli di avvio ed è consigliabile ri-valutare/popolare nuovamente gli indirizzi durante il ciclo di avvio successivo.

> [!NOTE]
> Gli oggetti di indirizzo delle parole chiave dinamiche AutoResolve attivano le notifiche in [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) e [**FWDeleteDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)ma non [**in FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

## <a name="non-autoresolve-dynamic-keyword-addresses"></a>Indirizzi di parole chiave dinamiche non risolvibili automaticamente

Il secondo tipo è *non AutoResolve*, dove il campo della parola chiave è qualsiasi stringa e gli indirizzi vengono definiti in fase di creazione. 

Questi oggetti vengono usati per archiviare un set di indirizzi IP, subnet o intervalli. Il *campo della* parola chiave qui viene usato per praticità di gestione e può essere impostato su qualsiasi stringa. Al *momento della* creazione, il campo addresses deve essere diverso da NULL. Gli indirizzi per questi oggetti vengono resi persistenti tra i riavvii.

> [!NOTE]
> Gli oggetti indirizzo dinamico non AutoResolve attivano le notifiche in [**FWAddDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)e [**FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

## <a name="more-about-dynamic-keyword-addresses"></a>Altre informazioni sugli indirizzi delle parole chiave dinamiche 

Tutti gli indirizzi delle parole chiave dinamiche devono avere un [**identificatore GUID univoco**](/windows/win32/api/guiddef/ns-guiddef-guid) per rappresentarli.

[**L'API FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) recapita notifiche a un client quando cambiano gli indirizzi delle parole chiave dinamiche. Non viene recapitato alcun payload al client che descriva esattamente cosa è cambiato nel sistema. Se è necessario conoscere gli oggetti modificati, è necessario eseguire una query sullo stato corrente degli oggetti nel sistema usando le API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) o [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) È possibile usare i vari flag per richiedere notifiche solo per un subset di oggetti. Se non si usano flag, le notifiche di modifica verranno recapitate per tutti gli oggetti.

Una regola del firewall può usare indirizzi di parole chiave dinamici invece di definire in modo esplicito gli indirizzi IP per la condizione di indirizzo remoto. Una regola del firewall può usare sia indirizzi di parole chiave dinamiche che intervalli di indirizzi remoti definiti in modo statico. Un singolo oggetto indirizzo di parola chiave dinamico può essere usato di nuovo in più regole del firewall. Se una regola del firewall non dispone di indirizzi remoti configurati, ovvero configurati solo con oggetti AutoResolve che non sono ancora stati risolti, la regola non verrà applicata. Inoltre, se una regola usa più indirizzi di parole chiave dinamici, la regola verrà applicata per tutti gli indirizzi attualmente risolti, anche se sono presenti altri oggetti che non sono ancora stati risolti. Quando un indirizzo di parola chiave dinamico viene aggiornato, anche tutti gli oggetti regola associati avranno i relativi indirizzi remoti aggiornati.

Il sistema operativo non applica alcuna dipendenza tra una regola e un indirizzo di parola chiave dinamico. Ciò significa che entrambi gli oggetti possono essere creati prima che la regola possa fare riferimento a ID di indirizzi di parole chiave dinamici che non esistono ancora (in questo caso, la regola non &mdash; verrà applicata). Inoltre, è possibile eliminare un indirizzo di parola chiave dinamico anche se è in uso da una regola del firewall. Questo argomento illustra come un amministratore può configurare le regole per l'uso dell'indirizzo dinamico delle parole chiave.

## <a name="code-examples"></a>Esempi di codice

Per provare ognuno di questi esempi di codice, avviare prima Visual Studio e creare un nuovo progetto basato sul modello di progetto **App** console. È sufficiente sostituire il contenuto di con `main.cpp` l'elenco di codice.

La maggior parte degli esempi di codice usa le [librerie di implementazione di Windows (WIL).](https://github.com/Microsoft/wil) Un modo pratico per installare WIL è passare  a Visual Studio, fare clic su Project Manage \> **NuGet Packages...** Sfoglia, digitare o \> incollare **Microsoft.Windows.ImplementationLibrary** nella casella di ricerca, selezionare l'elemento nei risultati della ricerca e quindi fare clic su **Installa** per installare il pacchetto per il progetto.

> [!NOTE]
> I tipi di puntatore per le funzioni gratuite di NetFw vengono pubblicati tramite , ma non viene pubblicata una libreria a `NetFw.h` collegamento statico. Usare il modello GetProcAddress [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)per / [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) chiamare queste funzioni, come illustrato in questi esempi di codice.

### <a name="add-a-dynamic-keyword-address"></a>Aggiungere un indirizzo di parola chiave dinamico

Questo esempio illustra come usare la [**funzione FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a>Eliminare un indirizzo di parola chiave dinamico

Questo esempio illustra come usare la [**funzione FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a>Enumerare e liberare gli indirizzi delle parole chiave dinamiche in base all'ID

Questo esempio illustra come usare le [**funzioni FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a>Enumerare e liberare gli indirizzi delle parole chiave dinamiche per tipo

Questo esempio illustra come usare le [**funzioni FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a>Aggiornare gli indirizzi delle parole chiave dinamiche

Questo esempio illustra come usare la [**funzione FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a>Sottoscrivere e gestire le notifiche dinamiche di modifica degli indirizzi delle parole chiave

Questo esempio illustra come usare le funzioni [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) e [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) e il [**callback**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) FWPM_DYNAMIC_KEYWORD_CALLBACK0.

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento per le parole chiave dinamiche del firewall](firewall-dynamic-keywords-reference.md)
