---
description: In questa sezione viene descritta la struttura di qualità del servizio (QOS) specifica del protocollo per ATM, che è contenuto nel campo ProviderSpecific della struttura QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Estensione QoS ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129106"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="75694-103">Estensione QoS ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="75694-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="75694-104">In questa sezione viene descritta la struttura di qualità del servizio ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) specifica del protocollo per ATM, che è contenuto nel campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) della struttura **QoS** .</span><span class="sxs-lookup"><span data-stu-id="75694-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="75694-105">Si noti che l'utilizzo di questa struttura **QoS** specifica di ATM è facoltativo per i client Windows Sockets 2 e che il provider di servizi ATM è necessario per eseguire il mapping della struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) generica agli elementi di informazioni Q. 2931 appropriati.</span><span class="sxs-lookup"><span data-stu-id="75694-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="75694-106">Tuttavia, se vengono specificate sia la struttura **FLOWSPEC** generica che la struttura **QoS** specifica di ATM, il valore specificato nella struttura **QoS** specifica di ATM avrà la precedenza in caso di conflitti.</span><span class="sxs-lookup"><span data-stu-id="75694-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="75694-107">Vedere la sezione 2,7 della specifica dell'API di Windows Sockets 2 per altre informazioni sulle disposizioni QoS e sulla struttura **FLOWSPEC** .</span><span class="sxs-lookup"><span data-stu-id="75694-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="75694-108">La struttura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) specifica del protocollo per ATM è una concatenazione di strutture dell'elemento informazioni Q. 2931, definite nel testo seguente.</span><span class="sxs-lookup"><span data-stu-id="75694-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="75694-109">Se un'applicazione omette un IE che UNI 3. x impone, il provider di servizi deve inserire un valore predefinito ragionevole, prendendo in considerazione le informazioni contenute nella struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) , se applicabile.</span><span class="sxs-lookup"><span data-stu-id="75694-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="75694-110">La gestione di IEs ripetute dipende dallo stesso IE.</span><span class="sxs-lookup"><span data-stu-id="75694-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="75694-111">Se un IE viene ripetuto ed è uno che può essere ripetuto in base alla specifica UNI del forum ATM, il provider deve gestirlo correttamente.</span><span class="sxs-lookup"><span data-stu-id="75694-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="75694-112">In questo caso, l'ordine nell'elenco determina l'ordine delle preferenze, con la preferenza per gli elementi visualizzati in precedenza nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="75694-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="75694-113">Se un IE viene ripetuto e questa operazione non è consentita per la specifica UNI del forum ATM, il provider potrebbe non riuscire a eseguire la richiesta dal client (opzione preferita) o usare l'ultimo IE di quel tipo trovato.</span><span class="sxs-lookup"><span data-stu-id="75694-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="75694-114">Ogni singola struttura di IE viene formattata nel modo seguente e identificata dal campo **IEType** :</span><span class="sxs-lookup"><span data-stu-id="75694-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="75694-115">I valori validi per il campo **IEType** sono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="75694-115">Legal values for the **IEType** field are defined as:</span></span>

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

<span data-ttu-id="75694-116">Il campo **IE** viene sovrapposto a una struttura di IE specifica e il campo **IELength** è la lunghezza totale, in byte, della struttura di IE, inclusi i campi **IEType** e **IELength** .</span><span class="sxs-lookup"><span data-stu-id="75694-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="75694-117">La semantica e i valori validi per ogni elemento di queste strutture IE sono per ogni specifica ATM UNI 3. x.</span><span class="sxs-lookup"><span data-stu-id="75694-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="75694-118">È \_ \_ possibile usare il campo SAP assente per gli elementi facoltativi per una determinata struttura di IE, per ogni specifica ATM UNI 3. x.</span><span class="sxs-lookup"><span data-stu-id="75694-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
