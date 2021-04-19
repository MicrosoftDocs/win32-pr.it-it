---
description: Nell'elenco seguente sono inclusi i metodi di indirizzi di CMSP interni.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Metodi helper interni di CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319882"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="043a2-103">Metodi helper interni di CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="043a2-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="043a2-104">Metodi helper interni di CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="043a2-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="043a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="043a2-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="043a2-106">**GetStaticTerminals**</span><span class="sxs-lookup"><span data-stu-id="043a2-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="043a2-107">Chiamato da [**get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) e [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) per ottenere una matrice di terminali statici che possono essere usati in questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="043a2-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="043a2-108">**GetDynamicTerminalClasses**</span><span class="sxs-lookup"><span data-stu-id="043a2-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="043a2-109">Chiamato da [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) e [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) per ottenere una matrice di classi di terminali dinamici che possono essere utilizzate per questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="043a2-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="043a2-110">**UpdateTerminalList**</span><span class="sxs-lookup"><span data-stu-id="043a2-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="043a2-111">Popola l'elenco di terminali statici del MSP.</span><span class="sxs-lookup"><span data-stu-id="043a2-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="043a2-112">**ReceiveTSPAddressData**</span><span class="sxs-lookup"><span data-stu-id="043a2-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="043a2-113">Chiamato quando un messaggio di dati di un TSP deve essere elaborato dall'indirizzo anziché da una chiamata specifica.</span><span class="sxs-lookup"><span data-stu-id="043a2-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="043a2-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="043a2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="043a2-115">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="043a2-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
