---
title: Classi helper estendibili di diagnostica wireless 802,11
description: L'infrastruttura di diagnostica wireless incorporata ha due punti di estensione. Supporto per l'helper ClassPurposeRevised Native Wi-Fi (RNWF) di helper ClassDiagnoses correlati a 802,11 estensioni di connettività.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516633"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="c7cb6-103">Classi helper estendibili di diagnostica wireless 802,11</span><span class="sxs-lookup"><span data-stu-id="c7cb6-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="c7cb6-104">L'infrastruttura di diagnostica wireless incorporata ha due punti di estensione.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="c7cb6-105">Classe helper padre</span><span class="sxs-lookup"><span data-stu-id="c7cb6-105">Parent Helper Class</span></span>                                | <span data-ttu-id="c7cb6-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="c7cb6-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c7cb6-107">Classe helper estendibile WiFi nativa (RNWF) modificata</span><span class="sxs-lookup"><span data-stu-id="c7cb6-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="c7cb6-108">Consente di diagnosticare i problemi relativi alle estensioni di connettività 802,11.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="c7cb6-109">Classe helper estendibile L2Security</span><span class="sxs-lookup"><span data-stu-id="c7cb6-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="c7cb6-110">Consente di diagnosticare i problemi relativi alle estensioni del protocollo di sicurezza di livello 2.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="c7cb6-111">Una classe helper di terze parti deve eseguire la registrazione con entrambe le classi helper padre per assicurarsi che venga chiamata la classe di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="c7cb6-112">Per ulteriori informazioni sulla registrazione, vedere la pagina relativa alla registrazione delle [estensioni di classe helper NDF](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c7cb6-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="c7cb6-113">Classe helper estendibile RNWF</span><span class="sxs-lookup"><span data-stu-id="c7cb6-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="c7cb6-114">Nome classe helper padre</span><span class="sxs-lookup"><span data-stu-id="c7cb6-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="c7cb6-115">La classe helper estendibile RNWF (WiFi native) modificata è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi correlati all'estensione di protocolli 802,11 utilizzati dal Wi-Fi nativo.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="c7cb6-116">I due attributi chiave forniti dalla classe helper RNWF sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="c7cb6-117">GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **al \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="c7cb6-118">Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo in \_ \_ stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="c7cb6-119">Questa stringa è in realtà un buffer della \_ \_ \_ struttura di ID WLAN WDIAG IHV definita in Wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="c7cb6-120">Questa struttura viene definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-120">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="c7cb6-121">**WDIAG \_ La \_ \_ sicurezza del flag ID WLAN IHV \_ \_ \_ abilitato** è l'unico valore **dwFlags** possibile.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="c7cb6-122">L'attributo corrispondente per la classe helper di terze parti deve corrispondere all'ID del servizio del modulo software corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="c7cb6-123">Questo è lo stesso nome che la terza parte deve essere registrata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="c7cb6-124">La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="c7cb6-125">Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata, quindi la chiama.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="c7cb6-126">Nella tabella seguente sono elencati gli attributi corrispondenti per la classe helper estensibile RNWF.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="c7cb6-127">Nome</span><span class="sxs-lookup"><span data-stu-id="c7cb6-127">Name</span></span>          | <span data-ttu-id="c7cb6-128">Type</span><span class="sxs-lookup"><span data-stu-id="c7cb6-128">Type</span></span>    | <span data-ttu-id="c7cb6-129">valore</span><span class="sxs-lookup"><span data-stu-id="c7cb6-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="c7cb6-130">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="c7cb6-130">DiagnosticsID</span></span> | <span data-ttu-id="c7cb6-131">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c7cb6-131">REG\_SZ</span></span> | <span data-ttu-id="c7cb6-132">\[\_Stringa GUID \_ DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="c7cb6-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="c7cb6-133">Classe helper estendibile L2Security</span><span class="sxs-lookup"><span data-stu-id="c7cb6-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="c7cb6-134">Nome classe helper padre</span><span class="sxs-lookup"><span data-stu-id="c7cb6-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="c7cb6-135">La classe helper Extensible Layer 2 Security (L2Security) è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi relativi ai servizi e ai moduli software corrispondenti che sostituiscono la funzionalità di sicurezza di livello 2.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="c7cb6-136">I due attributi chiave forniti dalla classe helper di sicurezza di livello 2 sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="c7cb6-137">GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **al \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="c7cb6-138">Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo in \_ \_ stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="c7cb6-139">Questa stringa è in realtà un buffer della \_ \_ \_ struttura di ID WLAN WDIAG IHV definita in wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="c7cb6-140">Questa struttura viene definita come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-140">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="c7cb6-141">**WDIAG \_ La \_ \_ sicurezza del flag ID WLAN IHV \_ \_ \_ abilitato** è l'unico valore **dwFlags** possibile.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="c7cb6-142">L'attributo corrispondente per la classe helper di terze parti deve corrispondere all'ID del servizio del modulo software corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="c7cb6-143">Questo è lo stesso nome che la terza parte deve essere registrata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="c7cb6-144">La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="c7cb6-145">Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata, quindi la chiama.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="c7cb6-146">Nella tabella seguente sono elencati gli attributi corrispondenti per la classe di supporto estensibile di sicurezza di livello 2.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="c7cb6-147">Nome</span><span class="sxs-lookup"><span data-stu-id="c7cb6-147">Name</span></span>          | <span data-ttu-id="c7cb6-148">Type</span><span class="sxs-lookup"><span data-stu-id="c7cb6-148">Type</span></span>    | <span data-ttu-id="c7cb6-149">valore</span><span class="sxs-lookup"><span data-stu-id="c7cb6-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="c7cb6-150">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="c7cb6-150">DiagnosticsID</span></span> | <span data-ttu-id="c7cb6-151">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c7cb6-151">REG\_SZ</span></span> | <span data-ttu-id="c7cb6-152">\[\_Stringa GUID \_ DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="c7cb6-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="c7cb6-153">Attributi corrispondenti</span><span class="sxs-lookup"><span data-stu-id="c7cb6-153">Matching Attributes</span></span>

<span data-ttu-id="c7cb6-154">**DiagnosticsID**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-154">**DiagnosticsID**</span></span>

<span data-ttu-id="c7cb6-155">802,11 diagnostica wireless eseguirà una query sul *DiagnosticsID* dal servizio Wi-Fi nativo di base per verificare se sono installate e incluse nella connessione eventuali moduli di sicurezza o estensioni wireless di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="c7cb6-156">La diagnostica senza fili fornirà quindi le ipotesi alle classi helper di terze parti usando *DiagnosticsID* come attributo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="c7cb6-157">Tutte le classi helper di terze parti devono essere incluse in e installate con il pacchetto driver associato.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="c7cb6-158">Il *DiagnosticsID* verrà definito nel file inf di miniport come chiave del registro di sistema nella direttiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c7cb6-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="c7cb6-159">Questa chiave definisce l'ID della classe helper wireless per il modulo software di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="c7cb6-160">Questa chiave è facoltativa per il Framework di estendibilità, ma è necessaria se l'implementazione include una classe helper wireless IHV che si connette a NDF ed è in grado di diagnosticare i problemi di connettività correlati alle estensioni wireless o di sicurezza RNWF.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="c7cb6-161">Le classi helper MS WLAN Diagnostics eseguiranno una query su questo ID dal servizio configurazione automatica senza fili quando vengono installati i moduli IHV e forniranno questo ID come riferimento o attributo corrispondente a NDF durante una sessione di diagnostica in modo che NDF possa chiamare la classe helper wireless di terze parti appropriata quando necessario.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="c7cb6-162">**\[\_Stringa GUID \_ DiagnosticsID\]**</span><span class="sxs-lookup"><span data-stu-id="c7cb6-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="c7cb6-163">Questo valore deve essere una stringa di tutte le lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="c7cb6-164">Ad esempio, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span><span class="sxs-lookup"><span data-stu-id="c7cb6-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="c7cb6-165">Ambito delle classi helper di diagnostica wireless 802,11</span><span class="sxs-lookup"><span data-stu-id="c7cb6-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="c7cb6-166">802,11 le classi helper di diagnostica wireless attualmente diagnosticano i problemi wireless nelle aree seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="c7cb6-167">Eventuali problemi di connettività 802,11 tra cui 802,11 Association, 802,11 Authentication, 802,11 impostazioni di sicurezza relative agli standard 802,11 & protocolli supportati in modo nativo nel sistema operativo e problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="c7cb6-168">Problemi di sicurezza di livello 2 per quanto concerne le configurazioni 802.1 x e i problemi correlati all'autenticazione di livello 2 usando i metodi supportati in modo nativo in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="c7cb6-169">Configurazione non corrispondente nelle impostazioni del profilo tra il client e il punto di accesso o l'infrastruttura e i servizi di rete.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="c7cb6-170">802,11 le classi helper di diagnostica wireless attualmente non diagnosticano i problemi wireless nelle aree seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="c7cb6-171">Problemi correlati alle estensioni 802,11 di terze parti, incluse le impostazioni del profilo o del driver correlate a tali estensioni.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="c7cb6-172">Problemi relativi ai metodi EAP di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="c7cb6-173">Problemi del driver miniport wireless.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="c7cb6-174">Qualsiasi protocollo di sicurezza 802,11 e di livello 2 o problemi relativi agli standard che non sono supportati in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="c7cb6-175">Problemi a livello di sistema o di componente che potrebbero influisca sulla connettività wireless, ad esempio risparmio energia, spazio su disco insufficiente, condizioni di memoria e problemi hardware.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="c7cb6-176">Inoltre, la diagnostica wireless 802,11 non analizza i case [**utilizzo del**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) .</span><span class="sxs-lookup"><span data-stu-id="c7cb6-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="c7cb6-177">I problemi di prestazioni wireless identificati verranno analizzati e segnalati come casi [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .</span><span class="sxs-lookup"><span data-stu-id="c7cb6-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




