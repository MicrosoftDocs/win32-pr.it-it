---
description: Quando viene installato un provider di rete, l'applicazione deve creare le chiavi del registro di sistema e i valori descritti in questo argomento.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chiavi del registro di sistema di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967720"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="6b274-103">Chiavi del registro di sistema di autenticazione</span><span class="sxs-lookup"><span data-stu-id="6b274-103">Authentication Registry Keys</span></span>

<span data-ttu-id="6b274-104">Quando viene installato un provider di rete, l'applicazione deve creare le chiavi del registro di sistema e i valori descritti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="6b274-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="6b274-105">Queste chiavi e i valori forniscono informazioni a MPR sui provider di rete installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6b274-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="6b274-106">L'MPR controlla queste chiavi all'avvio e carica le dll del provider di rete trovate.</span><span class="sxs-lookup"><span data-stu-id="6b274-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="6b274-107">Prima di creare un set di chiavi che contenga le informazioni sul provider di rete, è necessario aggiungere il nome del provider di rete alla chiave dell' **ordine** .</span><span class="sxs-lookup"><span data-stu-id="6b274-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="6b274-108">Questa chiave è una sottochiave della chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="6b274-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="6b274-109">La chiave **Order** contiene un solo valore, **ProviderOrder**, che elenca i provider installati e specifica l'ordine in cui devono essere tentati durante le operazioni che consentono di scorrere i provider fino a quando non viene trovato un provider di accettazione.</span><span class="sxs-lookup"><span data-stu-id="6b274-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="6b274-110">Il valore **ProviderOrder** contiene un elenco delimitato da virgole di nomi di chiave.</span><span class="sxs-lookup"><span data-stu-id="6b274-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="6b274-111">Ogni nome di chiave in **ProviderOrder** identifica un provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6b274-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="6b274-112">Quando MPR scorre i provider, li chiama nell'ordine in cui sono visualizzati nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="6b274-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="6b274-113">Il nome del provider impostato in **ProviderOrder** deve essere usato anche come nome della chiave del registro di sistema che contiene informazioni su tale provider.</span><span class="sxs-lookup"><span data-stu-id="6b274-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="6b274-114">Le chiavi del registro di sistema specifiche del provider vengono create come sottochiavi della chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="6b274-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="6b274-115">In altre parole, i nomi di provider specificati in **ProviderOrder** sono il percorso del registro di sistema delle chiavi specifiche del provider di rete, relativo al percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="6b274-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="6b274-116">Quando il servizio provider di rete è installato, l'applicazione di installazione deve aggiungere una chiave come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6b274-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="6b274-117">Dove *providerName* è il nome del provider di rete, come specificato nel valore **ProviderOrder** della chiave **Order** .</span><span class="sxs-lookup"><span data-stu-id="6b274-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="6b274-118">Il valore del **gruppo** sotto la chiave *providerName* deve essere impostato su "NetworkProvider".</span><span class="sxs-lookup"><span data-stu-id="6b274-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="6b274-119">Identifica il servizio come nel gruppo provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6b274-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="6b274-120">È inoltre necessario creare una sottochiave di *providerName*, **NetworkProvider**.</span><span class="sxs-lookup"><span data-stu-id="6b274-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="6b274-121">Questa chiave contiene i valori seguenti che descrivono il provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6b274-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="6b274-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6b274-122">Value</span></span>                       | <span data-ttu-id="6b274-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b274-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b274-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6b274-124">**Name**</span></span><br/>         | <span data-ttu-id="6b274-125">Contiene il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="6b274-125">Contains the name of the provider.</span></span> <span data-ttu-id="6b274-126">Questo nome viene visualizzato all'utente come nome della rete nelle finestre di dialogo di esplorazione e deve corrispondere al campo **lpProvider** restituito nelle strutture [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="6b274-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="6b274-127">Questo nome deve essere una variante del nome del prodotto, preferibilmente con alcune indicazioni della società, in modo che sia chiaro e univoco.</span><span class="sxs-lookup"><span data-stu-id="6b274-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="6b274-128">"MS-LanMan", ad esempio, è un nome valido, mentre "NET" sarebbe una scelta scadente.</span><span class="sxs-lookup"><span data-stu-id="6b274-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="6b274-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="6b274-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="6b274-130">Contiene il percorso completo della DLL che implementa il provider di rete.</span><span class="sxs-lookup"><span data-stu-id="6b274-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="6b274-131">MPR chiama [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) su questo percorso.</span><span class="sxs-lookup"><span data-stu-id="6b274-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="6b274-132">I valori seguenti vengono usati solo dai provider di rete che supportano le funzioni di gestione delle credenziali, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span><span class="sxs-lookup"><span data-stu-id="6b274-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="6b274-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6b274-133">Value</span></span>                              | <span data-ttu-id="6b274-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b274-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b274-135">**Classe**</span><span class="sxs-lookup"><span data-stu-id="6b274-135">**Class**</span></span><br/>               | <span data-ttu-id="6b274-136">**DWORD** che identifica la classe, o tipo, della funzionalità del provider supportata da questo provider.</span><span class="sxs-lookup"><span data-stu-id="6b274-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="6b274-137">Quando appropriato, i valori possono essere Uniti dall'operatore **or** .</span><span class="sxs-lookup"><span data-stu-id="6b274-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="6b274-138">I valori validi per questo documento sono la classe di rete, la classe della \_ \_ \_ credenziale, la classe AUTHENT e la classe di \_ \_ \_ \_ \_ servizio \_ .</span><span class="sxs-lookup"><span data-stu-id="6b274-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="6b274-139">Sebbene un provider possa supportare la funzionalità di autenticazione primaria, verrà usato un altro metodo per determinare quale autenticatore è primario.</span><span class="sxs-lookup"><span data-stu-id="6b274-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="6b274-140">**Windows XP/2000:** Il cambio di autenticatori primari non è supportato, pertanto questo valore viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6b274-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="6b274-141">**AuthentProviderPath**</span><span class="sxs-lookup"><span data-stu-id="6b274-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="6b274-142">Si tratta del nome file completo per la DLL che esporta le funzioni di gestione delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6b274-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="6b274-143">Questo valore è utile, ma non obbligatorio, solo quando il provider viene identificato come una classe CREDENTIAL \_ o un \_ provider di \_ classi AUTHENT primario.</span><span class="sxs-lookup"><span data-stu-id="6b274-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="6b274-144">Se questo valore non è presente per un provider di questa classe, le funzioni di gestione delle credenziali dovrebbero essere esportate dalla DLL identificata dal valore ProviderPath.</span><span class="sxs-lookup"><span data-stu-id="6b274-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="6b274-145">Questo valore viene utilizzato solo se si desidera creare il pacchetto delle funzioni di rete e delle funzioni di gestione delle credenziali in DLL separate.</span><span class="sxs-lookup"><span data-stu-id="6b274-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="6b274-146">Oltre ai valori utilizzati per registrare i provider di rete e i gestori delle credenziali, è possibile aggiungere un valore al registro di sistema per registrare una DLL per ricevere le notifiche di connessione.</span><span class="sxs-lookup"><span data-stu-id="6b274-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="6b274-147">A tale scopo, creare un \_ valore reg Expand \_ SZ nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="6b274-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="6b274-148">Questo valore deve specificare il percorso di una DLL che implementa l' [API di notifica della connessione](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="6b274-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="6b274-149">Il nome di questo valore può essere qualsiasi elemento desiderato, purché non sia in conflitto con i nomi dei valori preesistenti.</span><span class="sxs-lookup"><span data-stu-id="6b274-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="6b274-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="6b274-150">Example</span></span>

<span data-ttu-id="6b274-151">Nell'esempio seguente vengono illustrate le chiavi del registro di sistema per un sistema in cui sono installati due provider di rete: LanmanWorkStation e AnotherNetSvc.</span><span class="sxs-lookup"><span data-stu-id="6b274-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="6b274-152">AnotherNetSvc è anche una gestione credenziali.</span><span class="sxs-lookup"><span data-stu-id="6b274-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="6b274-153">Nell'esempio i nomi delle chiavi sono in grassetto e i nomi di valore sono in corsivo.</span><span class="sxs-lookup"><span data-stu-id="6b274-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="6b274-154">**HKEY \_ \_** \\  \\  \\  \\  \\ **Ordine** NetworkProvider del controllo CurrentControlSet del computer locale</span><span class="sxs-lookup"><span data-stu-id="6b274-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="6b274-155">*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"</span><span class="sxs-lookup"><span data-stu-id="6b274-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="6b274-156">**HKEY \_ \_** \\  \\  \\  \\  \\ **Avvisi** NetworkProvider del controllo CurrentControlSet del computer locale</span><span class="sxs-lookup"><span data-stu-id="6b274-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="6b274-157">*MyNotifyApp* = "c: \\ Connect \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="6b274-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="6b274-158">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**</span><span class="sxs-lookup"><span data-stu-id="6b274-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="6b274-159">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="6b274-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="6b274-160">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="6b274-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="6b274-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="6b274-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="6b274-162">*Classe* = 0x00000001 ( \_ classe di rete \_ )</span><span class="sxs-lookup"><span data-stu-id="6b274-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="6b274-163">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**</span><span class="sxs-lookup"><span data-stu-id="6b274-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="6b274-164">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="6b274-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="6b274-165">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="6b274-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="6b274-166">*Name* = "un'altra rete"*ProviderPath* = "c: \\ un'altra \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="6b274-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="6b274-167">*Classe* = 0x00000003 (classe di rete di una classe di \_ \_ \| \_ credenziali \_ )</span><span class="sxs-lookup"><span data-stu-id="6b274-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="6b274-168">*AuthentProviderPath* = "c: \\ un'altra \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="6b274-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

