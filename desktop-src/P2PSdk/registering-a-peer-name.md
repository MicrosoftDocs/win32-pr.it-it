---
description: "Per registrare un nome peer, un'applicazione deve fornire le informazioni seguenti: indirizzo IP listPeer identityPeer nameIf un nome peer non è protetto, un'identità è facoltativa."
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrazione di un nome peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315444"
---
# <a name="registering-a-peer-name"></a><span data-ttu-id="89672-103">Registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="89672-103">Registering a Peer Name</span></span>

<span data-ttu-id="89672-104">Per registrare un nome peer, un'applicazione deve fornire le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="89672-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="89672-105">Elenco indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="89672-105">IP address list</span></span>
-   [<span data-ttu-id="89672-106">Identità peer</span><span class="sxs-lookup"><span data-stu-id="89672-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="89672-107">Nome peer</span><span class="sxs-lookup"><span data-stu-id="89672-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="89672-108">Se un nome peer non è protetto, un'identità è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="89672-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="89672-109">Se un'identità peer viene specificata come **null**, il protocollo PNRP (Peer Name Resolution Protocol) usa un'identità peer predefinita interna.</span><span class="sxs-lookup"><span data-stu-id="89672-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="89672-110">Registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="89672-110">Registering a Peer Name</span></span>

<span data-ttu-id="89672-111">Dopo aver identificato l'elenco di indirizzi IP, l'identità peer e il nome peer, l'applicazione può registrare un nome peer chiamando [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="89672-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="89672-112">Usare le linee guida riportate nelle sezioni seguenti di questo argomento per apportare le configurazioni necessarie ai parametri **WSASetService** e alla struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="89672-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="89672-113">Configurazione di WSASetService</span><span class="sxs-lookup"><span data-stu-id="89672-113">Configuring WSASetService</span></span>

<span data-ttu-id="89672-114">Quando un'applicazione chiama [**WSASetService**](pnrp-and-wsasetservice.md), i parametri devono essere configurati in base alle specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="89672-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="89672-115">il valore di *essOperation* deve essere **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="89672-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="89672-116">*dwFlags* deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="89672-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="89672-117">*lpqsRegInfo* deve puntare a una struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , che deve essere configurata usando le linee guida riportate nella sezione **configurazione di WSAQUERYSET** seguente di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="89672-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="89672-118">Configurazione di WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="89672-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="89672-119">La struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve essere configurata in base alle specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="89672-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="89672-120">**dwSize** deve specificare la dimensione della struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="89672-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="89672-121">**lpszServiceInstanceName** deve puntare al nome peer registrato.</span><span class="sxs-lookup"><span data-stu-id="89672-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="89672-122">**lpBlob** deve puntare a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="89672-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="89672-123">**lpcsaBuffer** deve puntare all'elenco indirizzi.</span><span class="sxs-lookup"><span data-stu-id="89672-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="89672-124">I membri rimanenti sono descritti in [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="89672-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="89672-125">Dopo la registrazione di un nome peer, le informazioni sono disponibili per l'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="89672-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="89672-126">Tuttavia, si verifica un ritardo tra l'ora di registrazione e la propagazione delle informazioni di registrazione ad altri nodi.</span><span class="sxs-lookup"><span data-stu-id="89672-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="89672-127">Durante questo periodo, gli altri nodi potrebbero non essere in grado di risolvere il peer appena registrato.</span><span class="sxs-lookup"><span data-stu-id="89672-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="89672-128">Esempio di registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="89672-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="89672-129">Il frammento di codice seguente illustra come registrare un nome peer fornendo le informazioni corrette quando si chiama [**WSASetService**](pnrp-and-wsasetservice.md) usando la struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="89672-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



