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
# <a name="required-firewall-exceptions-for-teredo"></a>Eccezioni del firewall richieste per Teredo

Per consentire a un'applicazione di ricevere il traffico Teredo, è necessario che l'applicazione riceva traffico IPv6 nel firewall host e che l'applicazione sia in grado di impostare il [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) dell'opzione socket su "livello di protezione \_ \_ senza restrizioni". Per abilitare questo tipo di scenario, è necessario implementare le eccezioni del firewall descritte in dettaglio in questo documento.

Le configurazioni del firewall seguenti sono necessarie per garantire l'interoperatività uniforme tra un firewall e Teredo:

-   Il firewall client deve consentire la risoluzione dei teredo.ipv6.microsoft.com.
-   Per assicurarsi che i client Teredo possano comunicare correttamente con il server Teredo, è necessario aprire la porta UDP 3544.
-   Il firewall deve recuperare le porte UDP dinamiche usate dal servizio Teredo nel computer locale chiamando la funzione [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . le porte pertinenti sono di tipo FWPM \_ System \_ Port \_ TEREDO. La funzione **FwpmSystemPortsGet0** deve essere implementata al posto delle funzioni [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) o [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) ora deprecate.
-   Il firewall consente al sistema di inviare e ricevere pacchetti UDP/IPv4 alla porta UDP 1900 nella subnet locale, in modo da consentire il flusso del traffico di individuazione UPnP e può migliorare la velocità di connettività.
    > [!Note]  
    > Se questa condizione non viene soddisfatta, è possibile che si verifichino problemi di compatibilità che coinvolgono la comunicazione tra determinati tipi NAT. in particolare tra NAT simmetrico e NAT con restrizioni. Sebbene i NAT simmetrici siano diffusi negli hotspot e i NAT limitati siano diffusi nelle sedi, le comunicazioni tra i due possono causare errori sul lato del NAT con restrizioni.

     

-   È necessario abilitare le eccezioni ICMPv6 in ingresso e in uscita "richiesta echo" e "risposta echo". Queste eccezioni sono necessarie per garantire che un client Teredo possa fungere da inoltro specifico dell'host Teredo. Un inoltro specifico dell'host Teredo può essere identificato dall'indirizzo IPv6 nativo aggiuntivo o da un indirizzo 6to4 fornito con l'indirizzo Teredo.

I firewall client devono supportare i messaggi di errore ICMPv6 seguenti e le funzioni di individuazione per RFC 4443:



| Codice    | Descrizione                                    |
|---------|------------------------------------------------|
| 135/136 | Richiesta e annuncio router adiacenti ICMPV6 |
| 133/134 | Richiesta e annuncio router          |
| 128/129 | Richiesta echo ICMPV6 e risposta                  |
| 1       | Destinazione non raggiungibile                        |
| 2       | Pacchetto troppo grande                               |
| 3       | Tempo superato                                  |
| 4       | Parametro non valido                              |



 

Se questi messaggi non possono essere consentiti in modo specifico, l'esenzione di tutti i messaggi ICMPv6 dovrebbe essere abilitata sul firewall. Inoltre, il firewall host può notare che i pacchetti classificati con i codici 135/136 o 133/134 provengono da o sono assegnati a, il servizio in modalità utente **iphlpsvc** e non dallo stack. Questi pacchetti non devono essere eliminati dal firewall host. Il servizio Teredo viene implementato principalmente all'interno del servizio helper IP "modalità utente".

Utilizzando l'API Windows Firewall [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) per enumerare tutte le regole con il flag di attraversamento perimetrale impostato, tutte le applicazioni che desiderano ascoltare il traffico non richiesto vengono enumerate per l'eccezione del firewall. Informazioni specifiche sull'uso dell'opzione attraversamento confini sono descritte in dettaglio in [ricezione di traffico non richiesto su Teredo](receiving-unsolicited-traffic-over-teredo.md).

I callback non sono associati al codice di enumerazione di esempio seguente. si consiglia vivamente ai firewall di terze parti di eseguire periodicamente l'enumerazione o ogni volta che il firewall rileva una nuova applicazione che tenta di passare attraverso il firewall.


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



 

 