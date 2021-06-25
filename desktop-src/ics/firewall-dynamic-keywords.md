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
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="59d1f-104">Parole chiave dinamiche del firewall</span><span class="sxs-lookup"><span data-stu-id="59d1f-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="59d1f-105">Usare le API delle parole chiave dinamiche del firewall per gestire *gli indirizzi delle parole chiave* dinamiche in [Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="59d1f-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="59d1f-106">Un indirizzo di parola chiave dinamico viene usato per creare un set di indirizzi IP a cui possono fare riferimento una o più regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="59d1f-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="59d1f-107">Gli indirizzi delle parole chiave dinamiche supportano sia IPv4 che IPv6.</span><span class="sxs-lookup"><span data-stu-id="59d1f-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="59d1f-108">Per il contenuto di riferimento sulle API per le API introdotte in questo argomento, vedere Informazioni di riferimento [sulle parole chiave dinamiche del firewall.](firewall-dynamic-keywords-reference.md)</span><span class="sxs-lookup"><span data-stu-id="59d1f-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="59d1f-109">Operazioni sugli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="59d1f-110">Con le API delle parole chiave dinamiche del firewall, è possibile eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="59d1f-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="59d1f-111">Aggiungere indirizzi di parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="59d1f-112">Eliminare gli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="59d1f-113">Enumerare gli indirizzi delle parole chiave dinamiche in base all'ID o al tipo</span><span class="sxs-lookup"><span data-stu-id="59d1f-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="59d1f-114">Aggiornare gli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="59d1f-115">Sottoscrivere e gestire le notifiche dinamiche di modifica degli indirizzi delle parole chiave</span><span class="sxs-lookup"><span data-stu-id="59d1f-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="59d1f-116">Sono disponibili esempi di codice per tutte queste operazioni più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="59d1f-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="59d1f-117">Dopo aver aggiunto un indirizzo di parola chiave dinamico, l'indirizzo persiste tra i riavvii.</span><span class="sxs-lookup"><span data-stu-id="59d1f-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="59d1f-118">Al termine dell'operazione, è necessario eliminare un indirizzo di parola chiave dinamico.</span><span class="sxs-lookup"><span data-stu-id="59d1f-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="59d1f-119">Esistono due classi di indirizzi di parole chiave dinamici, come descritto nelle due sezioni successive.</span><span class="sxs-lookup"><span data-stu-id="59d1f-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="59d1f-120">Risolvere automaticamente gli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="59d1f-121">Il primo tipo è *AutoResolve,* dove il campo della parola chiave rappresenta un nome risolvibile e gli indirizzi IP non sono definiti al momento della creazione. </span><span class="sxs-lookup"><span data-stu-id="59d1f-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="59d1f-122">Questi oggetti hanno lo scopo di risolvere automaticamente gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="59d1f-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="59d1f-123">Cio' non tramite un amministratore in fase di creazione dell'oggetto; né tramite il sistema operativo stesso.</span><span class="sxs-lookup"><span data-stu-id="59d1f-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="59d1f-124">Un componente esterno al servizio firewall deve eseguire la risoluzione degli indirizzi IP per questi oggetti e aggiornarli in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="59d1f-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="59d1f-125">L'implementazione di tale componente non rientra nell'ambito di questo contenuto.</span><span class="sxs-lookup"><span data-stu-id="59d1f-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="59d1f-126">Un indirizzo di parola chiave dinamico viene indicato come *AutoResolve* impostando il **flag** FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE nell'oggetto quando si chiama la [**funzione FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="59d1f-127">Il *campo della* parola chiave deve essere usato per rappresentare il valore risolto, ovvero un nome di dominio completo &mdash; (FQDN) o un nome host.</span><span class="sxs-lookup"><span data-stu-id="59d1f-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="59d1f-128">Il *campo addresses* deve inizialmente essere NULL per questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="59d1f-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="59d1f-129">Gli indirizzi IP di questi oggetti non saranno persistenti tra i cicli di avvio ed è consigliabile ri-valutare/popolare nuovamente gli indirizzi durante il ciclo di avvio successivo.</span><span class="sxs-lookup"><span data-stu-id="59d1f-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="59d1f-130">Gli oggetti di indirizzo delle parole chiave dinamiche AutoResolve attivano le notifiche in [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) e [**FWDeleteDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)ma non [**in FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="59d1f-131">Indirizzi di parole chiave dinamiche non risolvibili automaticamente</span><span class="sxs-lookup"><span data-stu-id="59d1f-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="59d1f-132">Il secondo tipo è *non AutoResolve*, dove il campo della parola chiave è qualsiasi stringa e gli indirizzi vengono definiti in fase di creazione. </span><span class="sxs-lookup"><span data-stu-id="59d1f-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="59d1f-133">Questi oggetti vengono usati per archiviare un set di indirizzi IP, subnet o intervalli.</span><span class="sxs-lookup"><span data-stu-id="59d1f-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="59d1f-134">Il *campo della* parola chiave qui viene usato per praticità di gestione e può essere impostato su qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="59d1f-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="59d1f-135">Al *momento della* creazione, il campo addresses deve essere diverso da NULL.</span><span class="sxs-lookup"><span data-stu-id="59d1f-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="59d1f-136">Gli indirizzi per questi oggetti vengono resi persistenti tra i riavvii.</span><span class="sxs-lookup"><span data-stu-id="59d1f-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="59d1f-137">Gli oggetti indirizzo dinamico non AutoResolve attivano le notifiche in [**FWAddDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)e [**FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="59d1f-138">Altre informazioni sugli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="59d1f-139">Tutti gli indirizzi delle parole chiave dinamiche devono avere un [**identificatore GUID univoco**](/windows/win32/api/guiddef/ns-guiddef-guid) per rappresentarli.</span><span class="sxs-lookup"><span data-stu-id="59d1f-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="59d1f-140">[**L'API FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) recapita notifiche a un client quando cambiano gli indirizzi delle parole chiave dinamiche.</span><span class="sxs-lookup"><span data-stu-id="59d1f-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="59d1f-141">Non viene recapitato alcun payload al client che descriva esattamente cosa è cambiato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="59d1f-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="59d1f-142">Se è necessario conoscere gli oggetti modificati, è necessario eseguire una query sullo stato corrente degli oggetti nel sistema usando le API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) o [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="59d1f-143">È possibile usare i vari flag per richiedere notifiche solo per un subset di oggetti.</span><span class="sxs-lookup"><span data-stu-id="59d1f-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="59d1f-144">Se non si usano flag, le notifiche di modifica verranno recapitate per tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="59d1f-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="59d1f-145">Una regola del firewall può usare indirizzi di parole chiave dinamici invece di definire in modo esplicito gli indirizzi IP per la condizione di indirizzo remoto.</span><span class="sxs-lookup"><span data-stu-id="59d1f-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="59d1f-146">Una regola del firewall può usare sia indirizzi di parole chiave dinamiche che intervalli di indirizzi remoti definiti in modo statico.</span><span class="sxs-lookup"><span data-stu-id="59d1f-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="59d1f-147">Un singolo oggetto indirizzo di parola chiave dinamico può essere usato di nuovo in più regole del firewall.</span><span class="sxs-lookup"><span data-stu-id="59d1f-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="59d1f-148">Se una regola del firewall non dispone di indirizzi remoti configurati, ovvero configurati solo con oggetti AutoResolve che non sono ancora stati risolti, la regola non verrà applicata.</span><span class="sxs-lookup"><span data-stu-id="59d1f-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="59d1f-149">Inoltre, se una regola usa più indirizzi di parole chiave dinamici, la regola verrà applicata per tutti gli indirizzi attualmente risolti, anche se sono presenti altri oggetti che non sono ancora stati risolti.</span><span class="sxs-lookup"><span data-stu-id="59d1f-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="59d1f-150">Quando un indirizzo di parola chiave dinamico viene aggiornato, anche tutti gli oggetti regola associati avranno i relativi indirizzi remoti aggiornati.</span><span class="sxs-lookup"><span data-stu-id="59d1f-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="59d1f-151">Il sistema operativo non applica alcuna dipendenza tra una regola e un indirizzo di parola chiave dinamico.</span><span class="sxs-lookup"><span data-stu-id="59d1f-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="59d1f-152">Ciò significa che entrambi gli oggetti possono essere creati prima che la regola possa fare riferimento a ID di indirizzi di parole chiave dinamici che non esistono ancora (in questo caso, la regola non &mdash; verrà applicata).</span><span class="sxs-lookup"><span data-stu-id="59d1f-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="59d1f-153">Inoltre, è possibile eliminare un indirizzo di parola chiave dinamico anche se è in uso da una regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="59d1f-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="59d1f-154">Questo argomento illustra come un amministratore può configurare le regole per l'uso dell'indirizzo dinamico delle parole chiave.</span><span class="sxs-lookup"><span data-stu-id="59d1f-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="59d1f-155">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="59d1f-155">Code examples</span></span>

<span data-ttu-id="59d1f-156">Per provare ognuno di questi esempi di codice, avviare prima Visual Studio e creare un nuovo progetto basato sul modello di progetto **App** console.</span><span class="sxs-lookup"><span data-stu-id="59d1f-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="59d1f-157">È sufficiente sostituire il contenuto di con `main.cpp` l'elenco di codice.</span><span class="sxs-lookup"><span data-stu-id="59d1f-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="59d1f-158">La maggior parte degli esempi di codice usa le [librerie di implementazione di Windows (WIL).](https://github.com/Microsoft/wil)</span><span class="sxs-lookup"><span data-stu-id="59d1f-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="59d1f-159">Un modo pratico per installare WIL è passare  a Visual Studio, fare clic su Project Manage \> **NuGet Packages...** Sfoglia, digitare o \> incollare **Microsoft.Windows.ImplementationLibrary** nella casella di ricerca, selezionare l'elemento nei risultati della ricerca e quindi fare clic su **Installa** per installare il pacchetto per il progetto.</span><span class="sxs-lookup"><span data-stu-id="59d1f-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="59d1f-160">I tipi di puntatore per le funzioni gratuite di NetFw vengono pubblicati tramite , ma non viene pubblicata una libreria a `NetFw.h` collegamento statico.</span><span class="sxs-lookup"><span data-stu-id="59d1f-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="59d1f-161">Usare il modello GetProcAddress [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)per / [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) chiamare queste funzioni, come illustrato in questi esempi di codice.</span><span class="sxs-lookup"><span data-stu-id="59d1f-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="59d1f-162">Aggiungere un indirizzo di parola chiave dinamico</span><span class="sxs-lookup"><span data-stu-id="59d1f-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="59d1f-163">Questo esempio illustra come usare la [**funzione FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

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

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="59d1f-164">Eliminare un indirizzo di parola chiave dinamico</span><span class="sxs-lookup"><span data-stu-id="59d1f-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="59d1f-165">Questo esempio illustra come usare la [**funzione FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

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

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="59d1f-166">Enumerare e liberare gli indirizzi delle parole chiave dinamiche in base all'ID</span><span class="sxs-lookup"><span data-stu-id="59d1f-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="59d1f-167">Questo esempio illustra come usare le [**funzioni FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

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

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="59d1f-168">Enumerare e liberare gli indirizzi delle parole chiave dinamiche per tipo</span><span class="sxs-lookup"><span data-stu-id="59d1f-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="59d1f-169">Questo esempio illustra come usare le [**funzioni FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

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

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="59d1f-170">Aggiornare gli indirizzi delle parole chiave dinamiche</span><span class="sxs-lookup"><span data-stu-id="59d1f-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="59d1f-171">Questo esempio illustra come usare la [**funzione FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="59d1f-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

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

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="59d1f-172">Sottoscrivere e gestire le notifiche dinamiche di modifica degli indirizzi delle parole chiave</span><span class="sxs-lookup"><span data-stu-id="59d1f-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="59d1f-173">Questo esempio illustra come usare le funzioni [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) e [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) e il [**callback**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) FWPM_DYNAMIC_KEYWORD_CALLBACK0.</span><span class="sxs-lookup"><span data-stu-id="59d1f-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="59d1f-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59d1f-174">Related topics</span></span>

* [<span data-ttu-id="59d1f-175">Informazioni di riferimento per le parole chiave dinamiche del firewall</span><span class="sxs-lookup"><span data-stu-id="59d1f-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
