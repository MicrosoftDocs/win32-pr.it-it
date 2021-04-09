---
title: Uso di RPC con proxy Winsock
description: Uso di RPC con proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047317"
---
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="04a51-103">Uso di RPC con proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="04a51-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="04a51-104">Il rilascio di Microsoft Internet Access Server includeva il proxy Winsock, una versione migliorata di Windows Sockets API versione 1,1.</span><span class="sxs-lookup"><span data-stu-id="04a51-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="04a51-105">Il proxy Winsock consente a un'applicazione Windows Sockets, in esecuzione in un client di rete privata, di comportarsi come se fosse connessa direttamente a un'applicazione server Internet remota.</span><span class="sxs-lookup"><span data-stu-id="04a51-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="04a51-106">Il server proxy Microsoft funge da host per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="04a51-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="04a51-107">Ciò significa che tutte le comunicazioni a livello di applicazione sono canalizzate tramite un singolo computer protetto, ovvero il computer gateway che esegue Microsoft Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="04a51-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="04a51-108">In genere, per i trasferimenti di pacchetti di datagramma, la DLL di trasporto RPC Ignora le funzioni [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fornite in Wsock32.dll e comunica direttamente con il driver di dispositivo sottostante.</span><span class="sxs-lookup"><span data-stu-id="04a51-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="04a51-109">In questo modo si migliora la velocità dei trasferimenti di pacchetti ma le funzionalità del proxy Winsock non sono disponibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="04a51-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="04a51-110">Ogni provider di protocollo di rete deve disporre di un GUID associato.</span><span class="sxs-lookup"><span data-stu-id="04a51-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="04a51-111">La libreria di runtime RPC confronta i GUID UDP e IPX con gli identificatori Microsoft noti.</span><span class="sxs-lookup"><span data-stu-id="04a51-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="04a51-112">Se non corrispondono, RPC usa automaticamente Winsock.</span><span class="sxs-lookup"><span data-stu-id="04a51-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="04a51-113">Un'altra funzionalità del proxy Winsock è la possibilità di emulare il protocollo di trasporto TCP sul trasporto Novell SPX quando nel computer client SPX non è installato TCP.</span><span class="sxs-lookup"><span data-stu-id="04a51-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="04a51-114">Per utilizzare questa funzionalità con le applicazioni RPC, modificare il registro di sistema in ogni computer client per aggiungere la voce seguente:</span><span class="sxs-lookup"><span data-stu-id="04a51-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="04a51-115">Modificare il registro di sistema in ogni computer server per aggiungere la voce seguente:</span><span class="sxs-lookup"><span data-stu-id="04a51-115">Edit the registry on each server computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="04a51-116">Per ulteriori informazioni sui protocolli di trasporto RPC, vedere [specifica delle sequenze di protocollo](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="04a51-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="04a51-117">Per ulteriori informazioni sul proxy Winsock, vedere la documentazione del prodotto per Microsoft Internet Access Server.</span><span class="sxs-lookup"><span data-stu-id="04a51-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="04a51-118">Windows 2000 non implementa le voci del registro di sistema **protocolli** e **ServerProtocols** .</span><span class="sxs-lookup"><span data-stu-id="04a51-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="04a51-119">Microsoft fornisce tutti i trasporti noti come parte della libreria di Runtime.</span><span class="sxs-lookup"><span data-stu-id="04a51-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="04a51-120">Pertanto, queste voci non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="04a51-120">Therefore, these entries are not necessary.</span></span>

 

 