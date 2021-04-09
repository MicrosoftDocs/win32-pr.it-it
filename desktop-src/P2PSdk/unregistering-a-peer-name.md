---
description: Quando si annulla la registrazione di un nome peer, viene rimosso un nome registrato da un Cloud PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Annullamento della registrazione di un nome peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967530"
---
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="fb8eb-103">Annullamento della registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="fb8eb-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="fb8eb-104">Quando si annulla la registrazione di un nome peer, viene rimosso un nome registrato da un Cloud PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="fb8eb-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="fb8eb-105">Annullamento della registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="fb8eb-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="fb8eb-106">Per annullare la registrazione di un nome peer, chiamare [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="fb8eb-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="fb8eb-107">Il valore del parametro *essOperation* deve essere **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="fb8eb-108">Usare le linee guida riportate nelle sezioni seguenti di questo argomento per apportare le configurazioni necessarie ai parametri **WSASetService** e alla struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="fb8eb-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="fb8eb-109">Configurazione di WSASetService</span><span class="sxs-lookup"><span data-stu-id="fb8eb-109">Configuring WSASetService</span></span>

<span data-ttu-id="fb8eb-110">Quando un'applicazione chiama [**WSASetService**](pnrp-and-wsasetservice.md), i parametri devono essere configurati in base alle specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb8eb-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="fb8eb-111">il valore di *essOperation* deve essere **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="fb8eb-112">*dwFlags* deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="fb8eb-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="fb8eb-113">*lpqsRegInfo* deve puntare a una struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , che deve essere configurata utilizzando le linee guida riportate nella sezione seguente di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="fb8eb-114">Configurazione di WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="fb8eb-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="fb8eb-115">La struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve essere configurata in base alle specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb8eb-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="fb8eb-116">**dwSize** deve specificare la dimensione della struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="fb8eb-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="fb8eb-117">**lpszServiceInstanceName** deve puntare al nome peer di cui viene annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="fb8eb-118">**lpBlob** deve puntare a una struttura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="fb8eb-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="fb8eb-119">**lpcsaBuffer** deve puntare all'elenco indirizzi.</span><span class="sxs-lookup"><span data-stu-id="fb8eb-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="fb8eb-120">I membri rimanenti sono descritti in [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="fb8eb-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="fb8eb-121">Esempio di annullamento della registrazione di un nome peer</span><span class="sxs-lookup"><span data-stu-id="fb8eb-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="fb8eb-122">Il frammento di codice seguente illustra come annullare la registrazione di un nome peer fornendo le informazioni corrette quando si chiama [**WSASetService**](pnrp-and-wsasetservice.md) usando la struttura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="fb8eb-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



