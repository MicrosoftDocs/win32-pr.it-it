---
description: XP1 \_ supportano \_ \_ \_ i parametri dell'attributo MultiPoint, XP1 Multipoint Control \_ Plan e XP1 \_ multipoint \_ data \_ plane nella struttura di informazioni WSAPROTOCOL di Winsock \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attributi nella struttura WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307050"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="34220-103">Attributi nella struttura delle informazioni di WSAPROTOCOL \_</span><span class="sxs-lookup"><span data-stu-id="34220-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="34220-104">A supporto della tassonomia descritta in precedenza, vengono usati tre parametri di attributo nella struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per distinguere rispettivamente gli schemi usati nel controllo e nei piani dati:</span><span class="sxs-lookup"><span data-stu-id="34220-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="34220-105">XP1 \_ supporta \_ multipoint con un valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i due parametri seguenti sono significativi.</span><span class="sxs-lookup"><span data-stu-id="34220-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="34220-106">\_ \_ \_ Il piano di controllo multipoint XP1 indica se il piano di controllo è radice (valore = 1) o non radice (valore = 0).</span><span class="sxs-lookup"><span data-stu-id="34220-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="34220-107">\_ \_ Il piano dati multipoint XP1 \_ indica se il piano dati è radice (valore = 1) o non radice (valore = 0).</span><span class="sxs-lookup"><span data-stu-id="34220-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="34220-108">Si noti che sono presenti due voci di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se un protocollo multipoint supporta sia i piani dati radice che quelli non radice, una voce per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="34220-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="34220-109">L'applicazione può usare [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) per individuare se le comunicazioni multipoint sono supportate per un determinato protocollo e, in tal caso, come sono supportate rispetto al controllo e ai piani dati, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="34220-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 
