---
title: Eccezioni del firewall richieste per Teredo
description: Per consentire a un'applicazione di ricevere il traffico Teredo, è necessario che l'applicazione riceva traffico IPv6 nel firewall host e che l'applicazione sia in grado di impostare il livello di protezione IPV6 dell'opzione socket \_ \_ su "livello di protezione \_ \_ senza restrizioni".
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300198"
---
# <a name="required-firewall-exceptions-for-teredo"></a><span data-ttu-id="a8623-103">Eccezioni del firewall richieste per Teredo</span><span class="sxs-lookup"><span data-stu-id="a8623-103">Required Firewall Exceptions for Teredo</span></span>

<span data-ttu-id="a8623-104">Per consentire a un'applicazione di ricevere il traffico Teredo, è necessario che l'applicazione riceva traffico IPv6 nel firewall host e che l'applicazione sia in grado di impostare il [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) dell'opzione socket su "livello di protezione \_ \_ senza restrizioni".</span><span class="sxs-lookup"><span data-stu-id="a8623-104">For an application to receive Teredo traffic, the application must be permitted to receive IPv6 traffic in the host firewall, and the application is required to set the socket option [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) to 'PROTECTION\_LEVEL\_UNRESTRICTED'.</span></span> <span data-ttu-id="a8623-105">Per abilitare questo tipo di scenario, è necessario implementare le eccezioni del firewall descritte in dettaglio in questo documento.</span><span class="sxs-lookup"><span data-stu-id="a8623-105">To enable this type of scenario, the firewall exceptions detailed in this document must be implemented.</span></span>

<span data-ttu-id="a8623-106">Le configurazioni del firewall seguenti sono necessarie per garantire l'interoperatività uniforme tra un firewall e Teredo:</span><span class="sxs-lookup"><span data-stu-id="a8623-106">The following firewall configurations are required to ensure smooth interoperation between a firewall and Teredo:</span></span>

-   <span data-ttu-id="a8623-107">Il firewall client deve consentire la risoluzione dei teredo.ipv6.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a8623-107">The client firewall must allow resolution of teredo.ipv6.microsoft.com.</span></span>
-   <span data-ttu-id="a8623-108">Per assicurarsi che i client Teredo possano comunicare correttamente con il server Teredo, è necessario aprire la porta UDP 3544.</span><span class="sxs-lookup"><span data-stu-id="a8623-108">UDP Port 3544 must be open to ensure that Teredo clients can successfully communicate with the Teredo server.</span></span>
-   <span data-ttu-id="a8623-109">Il firewall deve recuperare le porte UDP dinamiche usate dal servizio Teredo nel computer locale chiamando la funzione [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . le porte pertinenti sono di tipo FWPM \_ System \_ Port \_ TEREDO.</span><span class="sxs-lookup"><span data-stu-id="a8623-109">The firewall must retrieve dynamic UDP ports used by Teredo service on the local machine by calling the [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) function; relevant ports are of type FWPM\_SYSTEM\_PORT\_TEREDO.</span></span> <span data-ttu-id="a8623-110">La funzione **FwpmSystemPortsGet0** deve essere implementata al posto delle funzioni [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) o [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) ora deprecate.</span><span class="sxs-lookup"><span data-stu-id="a8623-110">The **FwpmSystemPortsGet0** function should be implemented in place of the now deprecated [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) or [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) functions.</span></span>
-   <span data-ttu-id="a8623-111">Il firewall consente al sistema di inviare e ricevere pacchetti UDP/IPv4 alla porta UDP 1900 nella subnet locale, in modo da consentire il flusso del traffico di individuazione UPnP e può migliorare la velocità di connettività.</span><span class="sxs-lookup"><span data-stu-id="a8623-111">The firewall permits the system to send and receive UDP/IPv4 packets to UDP port 1900 on the local subnet as this allows UPnP discovery traffic to flow and has the potential to improve connectivity rates.</span></span>
    > [!Note]  
    > <span data-ttu-id="a8623-112">Se questa condizione non viene soddisfatta, è possibile che si verifichino problemi di compatibilità che coinvolgono la comunicazione tra determinati tipi NAT. in particolare tra NAT simmetrico e NAT con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="a8623-112">If this condition is not met, the potential for scenarios to encounter compatibility issues involving communication between certain NAT types is introduced; specifically between Symmetric NATs and Restricted NATs.</span></span> <span data-ttu-id="a8623-113">Sebbene i NAT simmetrici siano diffusi negli hotspot e i NAT limitati siano diffusi nelle sedi, le comunicazioni tra i due possono causare errori sul lato del NAT con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="a8623-113">While Symmetric NATs are popular in hotspots and Restricted NATs are popular in homes, communication between the two has the potential to fault on the side of the Restricted NAT.</span></span>

     

-   <span data-ttu-id="a8623-114">È necessario abilitare le eccezioni ICMPv6 in ingresso e in uscita "richiesta echo" e "risposta echo".</span><span class="sxs-lookup"><span data-stu-id="a8623-114">Incoming and outgoing ICMPv6 "Echo Request" and "Echo Reply" exceptions must be enabled.</span></span> <span data-ttu-id="a8623-115">Queste eccezioni sono necessarie per garantire che un client Teredo possa fungere da inoltro specifico dell'host Teredo.</span><span class="sxs-lookup"><span data-stu-id="a8623-115">These exceptions are necessary to ensure that a Teredo client can act as a Teredo host-specific relay.</span></span> <span data-ttu-id="a8623-116">Un inoltro specifico dell'host Teredo può essere identificato dall'indirizzo IPv6 nativo aggiuntivo o da un indirizzo 6to4 fornito con l'indirizzo Teredo.</span><span class="sxs-lookup"><span data-stu-id="a8623-116">A Teredo host-specific relay can be identified by the additional native IPv6 address or a 6to4 address supplied with the Teredo address.</span></span>

<span data-ttu-id="a8623-117">I firewall client devono supportare i messaggi di errore ICMPv6 seguenti e le funzioni di individuazione per RFC 4443:</span><span class="sxs-lookup"><span data-stu-id="a8623-117">Client firewalls must support the following ICMPv6 error messages and discovery functions per RFC 4443:</span></span>



| <span data-ttu-id="a8623-118">Codice</span><span class="sxs-lookup"><span data-stu-id="a8623-118">Code</span></span>    | <span data-ttu-id="a8623-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8623-119">Description</span></span>                                    |
|---------|------------------------------------------------|
| <span data-ttu-id="a8623-120">135/136</span><span class="sxs-lookup"><span data-stu-id="a8623-120">135/136</span></span> | <span data-ttu-id="a8623-121">Richiesta e annuncio router adiacenti ICMPV6</span><span class="sxs-lookup"><span data-stu-id="a8623-121">ICMPV6 Neighbor Solicitation and Advertisement</span></span> |
| <span data-ttu-id="a8623-122">133/134</span><span class="sxs-lookup"><span data-stu-id="a8623-122">133/134</span></span> | <span data-ttu-id="a8623-123">Richiesta e annuncio router</span><span class="sxs-lookup"><span data-stu-id="a8623-123">Router Solicitation and Advertisement</span></span>          |
| <span data-ttu-id="a8623-124">128/129</span><span class="sxs-lookup"><span data-stu-id="a8623-124">128/129</span></span> | <span data-ttu-id="a8623-125">Richiesta echo ICMPV6 e risposta</span><span class="sxs-lookup"><span data-stu-id="a8623-125">ICMPV6 Echo Request and Reply</span></span>                  |
| <span data-ttu-id="a8623-126">1</span><span class="sxs-lookup"><span data-stu-id="a8623-126">1</span></span>       | <span data-ttu-id="a8623-127">Destinazione non raggiungibile</span><span class="sxs-lookup"><span data-stu-id="a8623-127">Destination Unreachable</span></span>                        |
| <span data-ttu-id="a8623-128">2</span><span class="sxs-lookup"><span data-stu-id="a8623-128">2</span></span>       | <span data-ttu-id="a8623-129">Pacchetto troppo grande</span><span class="sxs-lookup"><span data-stu-id="a8623-129">Packet Too Large</span></span>                               |
| <span data-ttu-id="a8623-130">3</span><span class="sxs-lookup"><span data-stu-id="a8623-130">3</span></span>       | <span data-ttu-id="a8623-131">Tempo superato</span><span class="sxs-lookup"><span data-stu-id="a8623-131">Time Exceeded</span></span>                                  |
| <span data-ttu-id="a8623-132">4</span><span class="sxs-lookup"><span data-stu-id="a8623-132">4</span></span>       | <span data-ttu-id="a8623-133">Parametro non valido</span><span class="sxs-lookup"><span data-stu-id="a8623-133">Invalid Parameter</span></span>                              |



 

<span data-ttu-id="a8623-134">Se questi messaggi non possono essere consentiti in modo specifico, l'esenzione di tutti i messaggi ICMPv6 dovrebbe essere abilitata sul firewall.</span><span class="sxs-lookup"><span data-stu-id="a8623-134">If these messages cannot be specifically allowed, then the exemption of all ICMPv6 messages should be enabled on the firewall.</span></span> <span data-ttu-id="a8623-135">Inoltre, il firewall host può notare che i pacchetti classificati con i codici 135/136 o 133/134 provengono da o sono assegnati a, il servizio in modalità utente **iphlpsvc** e non dallo stack.</span><span class="sxs-lookup"><span data-stu-id="a8623-135">Additionally, the host firewall may notice that the packets classified by codes 135/136 or 133/134 originate from, or are targeted to, the user mode service **iphlpsvc** and not from the stack.</span></span> <span data-ttu-id="a8623-136">Questi pacchetti non devono essere eliminati dal firewall host.</span><span class="sxs-lookup"><span data-stu-id="a8623-136">These packets must not be dropped by the host firewall.</span></span> <span data-ttu-id="a8623-137">Il servizio Teredo viene implementato principalmente all'interno del servizio helper IP "modalità utente".</span><span class="sxs-lookup"><span data-stu-id="a8623-137">The Teredo service is implemented primarily within the 'user mode' IP Helper service.</span></span>

<span data-ttu-id="a8623-138">Utilizzando l'API Windows Firewall [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) per enumerare tutte le regole con il flag di attraversamento perimetrale impostato, tutte le applicazioni che desiderano ascoltare il traffico non richiesto vengono enumerate per l'eccezione del firewall.</span><span class="sxs-lookup"><span data-stu-id="a8623-138">Using the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows Firewall API to enumerate all rules with the Edge Traversal flag set, all applications that want to listen for unsolicited traffic are enumerated for the firewall exception.</span></span> <span data-ttu-id="a8623-139">Informazioni specifiche sull'uso dell'opzione attraversamento confini sono descritte in dettaglio in [ricezione di traffico non richiesto su Teredo](receiving-unsolicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="a8623-139">Specific information regarding the use of the Edge Traversal option is detailed in [Receiving Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="a8623-140">I callback non sono associati al codice di enumerazione di esempio seguente. si consiglia vivamente ai firewall di terze parti di eseguire periodicamente l'enumerazione o ogni volta che il firewall rileva una nuova applicazione che tenta di passare attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="a8623-140">Callbacks are not associated with the following sample enumeration code; it is strongly recommended that third party firewalls perform the enumeration periodically, or whenever the firewall detects a new application attempting to go through the firewall.</span></span>


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 