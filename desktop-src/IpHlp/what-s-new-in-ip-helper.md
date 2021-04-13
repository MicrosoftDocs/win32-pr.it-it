---
description: Novità dell'helper IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Novità dell'helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c1a6eebb3e9e785e8988b822df0b2a80ae6eba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349016"
---
# <a name="whats-new-in-ip-helper"></a><span data-ttu-id="c0e3e-103">Novità dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="c0e3e-103">What's New in IP Helper</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="c0e3e-104">Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0e3e-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="c0e3e-105">Le funzionalità seguenti sono state aggiunte alle API helper IP in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-105">The following features have been added to the IP Helper APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="c0e3e-106">Funzione che recupera le stime della larghezza di banda cronologica per una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-106">A function that retrieves historical bandwidth estimates for a network connection.</span></span> <span data-ttu-id="c0e3e-107">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-107">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-108">**GetIpNetworkConnectionBandwidthEstimates**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-108">**GetIpNetworkConnectionBandwidthEstimates**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

<span data-ttu-id="c0e3e-109">Struttura che contiene informazioni sulle stime della larghezza di banda disponibili e la varianza associata come determinato dallo stack TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-109">A structure that contains information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.</span></span> <span data-ttu-id="c0e3e-110">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-110">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-111">**\_informazioni sulla larghezza di banda nl \_**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-111">**NL\_BANDWIDTH\_INFORMATION**</span></span>](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="c0e3e-112">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0e3e-112">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="c0e3e-113">Le funzionalità seguenti sono state aggiunte alle API helper IP in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-113">The following features have been added to the IP Helper APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="c0e3e-114">Funzioni che convertono un indirizzo Ethernet tra un formato binario e un formato di stringa per l'indirizzo MAC Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-114">Functions that convert an Ethernet address between a binary format and string format for the Ethernet MAC address.</span></span> <span data-ttu-id="c0e3e-115">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-115">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-116">**RtlEthernetAddressToString**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-116">**RtlEthernetAddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [<span data-ttu-id="c0e3e-117">**RtlEthernetStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-117">**RtlEthernetStringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="c0e3e-118">Windows Server 2008 e Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="c0e3e-118">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="c0e3e-119">Le funzioni seguenti sono state aggiunte alle API helper IP in Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c0e3e-119">The following functions have been added to the IP Helper APIs on Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="c0e3e-120">Funzione che funziona con IPv4 e il Internet Control Message Protocol (ICMP).</span><span class="sxs-lookup"><span data-stu-id="c0e3e-120">A function that works with IPv4 and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="c0e3e-121">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-121">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-122">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-122">**IcmpSendEcho2Ex**</span></span>](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a><span data-ttu-id="c0e3e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0e3e-123">Windows Vista</span></span>

<span data-ttu-id="c0e3e-124">Sono stati aggiunti i seguenti gruppi di funzioni alle API helper IP in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-124">The following groups of functions have been added to the IP Helper APIs on Windows Vista and later.</span></span>

<span data-ttu-id="c0e3e-125">Funzioni che funzionano con IPv6 e IPv4 per la conversione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-125">Functions that work with both IPv6 and IPv4 for interface conversion.</span></span> <span data-ttu-id="c0e3e-126">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-126">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-127">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-127">**ConvertInterfaceAliasToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="c0e3e-128">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-128">**ConvertInterfaceGuidToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="c0e3e-129">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-129">**ConvertInterfaceIndexToLuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="c0e3e-130">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-130">**ConvertInterfaceLuidToGuid**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="c0e3e-131">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-131">**ConvertInterfaceLuidToIndex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="c0e3e-132">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-132">**ConvertInterfaceLuidToNameA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="c0e3e-133">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-133">**ConvertInterfaceLuidToNameW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="c0e3e-134">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-134">**ConvertInterfaceNameToLuidA**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="c0e3e-135">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-135">**ConvertInterfaceNameToLuidW**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="c0e3e-136">**Se \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-136">**if\_indextoname**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="c0e3e-137">**Se \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-137">**if\_nametoindex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

<span data-ttu-id="c0e3e-138">Funzioni che funzionano con IPv6 e IPv4 per la gestione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-138">Functions that work with both IPv6 and IPv4 for interface management.</span></span> <span data-ttu-id="c0e3e-139">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-139">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-140">**GetIfEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="c0e3e-141">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-141">**GetIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="c0e3e-142">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-142">**GetIfTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="c0e3e-143">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-143">**GetIfTable2Ex**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="c0e3e-144">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-144">**GetInvertedIfStackTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="c0e3e-145">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-145">**GetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="c0e3e-146">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-146">**GetIpInterfaceTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="c0e3e-147">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-147">**InitializeIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="c0e3e-148">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-148">**SetIpInterfaceEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

<span data-ttu-id="c0e3e-149">Funzioni che funzionano con IPv6 e IPv4 per la gestione degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-149">Functions that work with both IPv6 and IPv4 for IP address management.</span></span> <span data-ttu-id="c0e3e-150">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-150">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-151">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-151">**CreateAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="c0e3e-152">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-152">**CreateUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="c0e3e-153">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-153">**DeleteAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="c0e3e-154">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-154">**DeleteUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="c0e3e-155">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-155">**GetAnycastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="c0e3e-156">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-156">**GetAnycastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="c0e3e-157">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-157">**GetMulticastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="c0e3e-158">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-158">**GetMulticastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="c0e3e-159">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-159">**GetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="c0e3e-160">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-160">**GetUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="c0e3e-161">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-161">**InitializeUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="c0e3e-162">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-162">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="c0e3e-163">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-163">**SetUnicastIpAddressEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

<span data-ttu-id="c0e3e-164">Funzione che funziona sia con IPv6 sia con IPv4 per la gestione della memoria della tabella IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-164">A function that works with both IPv6 and IPv4 for IP table memory management.</span></span> <span data-ttu-id="c0e3e-165">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-165">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-166">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-166">**FreeMibTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

<span data-ttu-id="c0e3e-167">Funzioni che funzionano con IPv6 e IPv4 per la gestione indirizzi IP adiacenti.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-167">Functions that work with both IPv6 and IPv4 for IP neighbor address management.</span></span> <span data-ttu-id="c0e3e-168">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-168">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-169">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-169">**CreateIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="c0e3e-170">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-170">**DeleteIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="c0e3e-171">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-171">**FlushIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="c0e3e-172">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-172">**GetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="c0e3e-173">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-173">**GetIpNetTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="c0e3e-174">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-174">**ResolveIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="c0e3e-175">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-175">**ResolveNeighbor**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="c0e3e-176">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-176">**SetIpNetEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

<span data-ttu-id="c0e3e-177">Funzioni che funzionano con IPv6 e IPv4 per la gestione dei percorsi IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-177">Functions that work with both IPv6 and IPv4 for IP path management.</span></span> <span data-ttu-id="c0e3e-178">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-178">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-179">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-179">**FlushIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="c0e3e-180">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-180">**GetIpPathEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="c0e3e-181">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-181">**GetIpPathTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

<span data-ttu-id="c0e3e-182">Funzioni che funzionano con IPv6 e IPv4 per la gestione delle route IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-182">Functions that work with both IPv6 and IPv4 for IP route management.</span></span> <span data-ttu-id="c0e3e-183">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-183">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-184">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-184">**CreateIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="c0e3e-185">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-185">**DeleteIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="c0e3e-186">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-186">**GetBestRoute2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="c0e3e-187">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-187">**GetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="c0e3e-188">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-188">**GetIpForwardTable2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="c0e3e-189">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-189">**InitializeIpForwardEntry**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="c0e3e-190">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-190">**SetIpForwardEntry2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="c0e3e-191">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-191">**SetIpStatisticsEx**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

<span data-ttu-id="c0e3e-192">Funzioni che funzionano con IPv6 e IPv4 per la notifica.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-192">Functions that work with both IPv6 and IPv4 for notification.</span></span> <span data-ttu-id="c0e3e-193">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-193">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-194">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-194">**CancelMibChangeNotify2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="c0e3e-195">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-195">**NotifyIpInterfaceChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="c0e3e-196">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-196">**NotifyRouteChange2**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="c0e3e-197">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-197">**NotifyUnicastIpAddressChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

<span data-ttu-id="c0e3e-198">Funzioni di utilità che funzionano con gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-198">Utility functions that work with IP addresses.</span></span> <span data-ttu-id="c0e3e-199">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-199">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-200">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-200">**ConvertIpv4MaskToLength**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="c0e3e-201">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-201">**ConvertLengthToIpv4Mask**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="c0e3e-202">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-202">**CreateSortedAddressPairs**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="c0e3e-203">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-203">**ParseNetworkString**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

<span data-ttu-id="c0e3e-204">Funzioni che funzionano con Transmission Control Protocol (TCP) e UDP (User Datagram Protocol) per recuperare la tabella di connessione TCP IPv6 o IPv4 o la tabella del listener UDP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-204">Functions that work with Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) to retrieve the IPv6 or IPv4 TCP connection table or UDP listener table.</span></span> <span data-ttu-id="c0e3e-205">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-205">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-206">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-206">**GetTcp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="c0e3e-207">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-207">**GetTcp6Table2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="c0e3e-208">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-208">**GetTcpTable2**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="c0e3e-209">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-209">**GetUdp6Table**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

<span data-ttu-id="c0e3e-210">Funzioni che funzionano con Transmission Control Protocol (TCP) per recuperare le statistiche TCP estese in una connessione.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-210">Functions that work with Transmission Control Protocol (TCP) to retrieve extended TCP statistics on a connection.</span></span> <span data-ttu-id="c0e3e-211">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-211">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-212">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-212">**GetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="c0e3e-213">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-213">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="c0e3e-214">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-214">**SetPerTcp6ConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="c0e3e-215">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-215">**SetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

<span data-ttu-id="c0e3e-216">Nuove funzioni che funzionano per la gestione client IPv6 Teredo.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-216">New functions that work for Teredo IPv6 client management.</span></span> <span data-ttu-id="c0e3e-217">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-217">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-218">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-218">**GetTeredoPort**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="c0e3e-219">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-219">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="c0e3e-220">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-220">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

<span data-ttu-id="c0e3e-221">Funzioni di utilità che forniscono conversioni tra gli indirizzi IP e le rappresentazioni di stringa degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-221">Utility functions that provide conversions between IP addresses and string representations of IP addresses.</span></span> <span data-ttu-id="c0e3e-222">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-222">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-223">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-223">**RtlIpv4AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="c0e3e-224">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-224">**RtlIpv4AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="c0e3e-225">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-225">**RtlIpv4StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="c0e3e-226">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-226">**RtlIpv4StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="c0e3e-227">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-227">**RtlIpv6AddressToString**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="c0e3e-228">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-228">**RtlIpv6AddressToStringEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="c0e3e-229">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-229">**RtlIpv6StringToAddress**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="c0e3e-230">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-230">**RtlIpv6StringToAddressEx**</span></span>](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

<span data-ttu-id="c0e3e-231">Funzioni che forniscono prenotazioni permanenti per un blocco consecutivo di porte TCP o UDP nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c0e3e-231">Functions that provide persistent reservations for a consecutive block of TCP or UDP ports on the local computer.</span></span> <span data-ttu-id="c0e3e-232">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-232">For more information, see:</span></span>

-   [<span data-ttu-id="c0e3e-233">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-233">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="c0e3e-234">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-234">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="c0e3e-235">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-235">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="c0e3e-236">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-236">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="c0e3e-237">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-237">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="c0e3e-238">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-238">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a><span data-ttu-id="c0e3e-239">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0e3e-239">Windows Server 2003</span></span>

<span data-ttu-id="c0e3e-240">Le funzioni seguenti sono state aggiunte alle API helper IP in Windows Server 2003 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-240">The following functions have been added to the IP Helper APIs on Windows Server 2003 and later:</span></span>

-   <span data-ttu-id="c0e3e-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0e3e-241">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="c0e3e-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0e3e-242">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

## <a name="windows-xp-sp2"></a><span data-ttu-id="c0e3e-243">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="c0e3e-243">Windows XP SP2</span></span>

<span data-ttu-id="c0e3e-244">Le funzioni seguenti sono state aggiunte alle API helper IP in Windows XP con Service Pack 2 (SP2) e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="c0e3e-244">The following functions have been added to the IP Helper APIs on Windows XP with Service Pack 2 (SP2) and later:</span></span>

-   [<span data-ttu-id="c0e3e-245">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-245">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="c0e3e-246">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-246">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="c0e3e-247">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-247">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="c0e3e-248">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="c0e3e-248">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
