---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funzioni helper in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306954"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="29587-103">Funzioni helper in SPI</span><span class="sxs-lookup"><span data-stu-id="29587-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="29587-104">**NSPGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="29587-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="29587-105">La funzione [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera le informazioni sullo schema della classe di servizio mantenute da un provider dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="29587-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="29587-106">Viene inoltre utilizzata dalla DLL di Windows Sockets 2 nell'implementazione di [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span><span class="sxs-lookup"><span data-stu-id="29587-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="29587-107">Le macro seguenti sono definite nel file di intestazione *Svcguid. h* e possono contribuire al mapping tra le classi di servizio note e questi spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="29587-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="29587-108">Nome macro</span><span class="sxs-lookup"><span data-stu-id="29587-108">Macro name</span></span>                                                                              | <span data-ttu-id="29587-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29587-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29587-110">**SVCID \_ TCP (porta)**</span><span class="sxs-lookup"><span data-stu-id="29587-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="29587-111">**\_UDP SVCID (porta)**</span><span class="sxs-lookup"><span data-stu-id="29587-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="29587-112">Data una porta TCP o UDP per il protocollo Internet, restituisce il GUID.</span><span class="sxs-lookup"><span data-stu-id="29587-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="29587-113">**\_SVCID \_ TCP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="29587-114">**\_UDP SVCID \_ (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="29587-115">Restituisce **true** se il GUID per TCP o UDP è compreso nell'intervallo consentito.</span><span class="sxs-lookup"><span data-stu-id="29587-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="29587-116">**PORTA \_ da \_ SVCID \_ TCP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="29587-117">**PORTA \_ da \_ SVCID \_ UDP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="29587-118">Restituisce la porta TCP o UDP associata al GUID.</span><span class="sxs-lookup"><span data-stu-id="29587-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="29587-119">**SVCID \_ NetWare (SAPI)**</span><span class="sxs-lookup"><span data-stu-id="29587-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="29587-120">Dato l'identificatore di Service Advertising Protocol (SAP), restituisce il GUID.</span><span class="sxs-lookup"><span data-stu-id="29587-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="29587-121">Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare.</span><span class="sxs-lookup"><span data-stu-id="29587-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="29587-122">**SAPIDO \_ da \_ SVCID \_ NetWare (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="29587-123">Restituisce l'identificatore SAP di NetWare associato al GUID.</span><span class="sxs-lookup"><span data-stu-id="29587-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="29587-124">Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare.</span><span class="sxs-lookup"><span data-stu-id="29587-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="29587-125">**è \_ SVCID \_ NetWare (Guid)**</span><span class="sxs-lookup"><span data-stu-id="29587-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="29587-126">Restituisce **true** se il GUID per NetWare è compreso nell'intervallo consentito.</span><span class="sxs-lookup"><span data-stu-id="29587-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="29587-127">Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare.</span><span class="sxs-lookup"><span data-stu-id="29587-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="29587-128">Il file di intestazione *Svcguid. h* non è incluso automaticamente nel file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="29587-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




