---
title: Funzioni helper IP
description: Le funzioni seguenti recuperano e modificano le impostazioni di configurazione per il trasporto TCP/IP nel computer locale.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ee16bb0b65545c4abbef387c5b90d42fb9d3c629
ms.sourcegitcommit: ea0069adb72dbfa717e73f3a96c3407a49ec0dab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/17/2021
ms.locfileid: "114394213"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="1e4a6-103">Funzioni helper IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-103">IP Helper functions</span></span>

<span data-ttu-id="1e4a6-104">Le funzioni seguenti recuperano e modificano le impostazioni di configurazione per il trasporto TCP/IP nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1e4a6-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="1e4a6-105">L'elenco categorico seguente consente di determinare quale raccolta di funzioni è più adatta per una determinata attività.</span><span class="sxs-lookup"><span data-stu-id="1e4a6-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="1e4a6-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="1e4a6-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="1e4a6-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="1e4a6-109">Gestione degli adapter</span><span class="sxs-lookup"><span data-stu-id="1e4a6-109">Adapter management</span></span>

-   [<span data-ttu-id="1e4a6-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="1e4a6-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="1e4a6-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="1e4a6-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="1e4a6-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="1e4a6-115">Gestione del protocollo ARP (Address Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="1e4a6-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="1e4a6-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="1e4a6-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="1e4a6-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="1e4a6-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="1e4a6-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="1e4a6-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="1e4a6-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="1e4a6-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="1e4a6-124">Conversione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="1e4a6-124">Interface conversion</span></span>

-   [<span data-ttu-id="1e4a6-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="1e4a6-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="1e4a6-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="1e4a6-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="1e4a6-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="1e4a6-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="1e4a6-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="1e4a6-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="1e4a6-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="1e4a6-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="1e4a6-135">**if \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="1e4a6-136">**if \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="1e4a6-137">Gestione delle interfacce</span><span class="sxs-lookup"><span data-stu-id="1e4a6-137">Interface management</span></span>

-   [<span data-ttu-id="1e4a6-138">**FreeInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-138">**FreeInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-freeinterfacednssettings)
-   [<span data-ttu-id="1e4a6-139">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-139">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="1e4a6-140">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-140">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="1e4a6-141">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-141">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="1e4a6-142">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-142">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="1e4a6-143">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-143">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="1e4a6-144">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-144">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="1e4a6-145">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-145">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="1e4a6-146">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-146">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="1e4a6-147">**GetInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-147">**GetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
-   [<span data-ttu-id="1e4a6-148">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-148">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="1e4a6-149">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-149">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="1e4a6-150">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-150">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="1e4a6-151">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-151">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="1e4a6-152">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-152">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="1e4a6-153">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-153">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="1e4a6-154">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-154">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="1e4a6-155">**SetInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-155">**SetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
-   [<span data-ttu-id="1e4a6-156">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-156">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="1e4a6-157">Ip (Internet Protocol) e Internet Control Message Protocol (ICMP)</span><span class="sxs-lookup"><span data-stu-id="1e4a6-157">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="1e4a6-158">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-158">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="1e4a6-159">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-159">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="1e4a6-160">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-160">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="1e4a6-161">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-161">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="1e4a6-162">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-162">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="1e4a6-163">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-163">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="1e4a6-164">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-164">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="1e4a6-165">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-165">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="1e4a6-166">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-166">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="1e4a6-167">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-167">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="1e4a6-168">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-168">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="1e4a6-169">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-169">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="1e4a6-170">Gestione indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-170">IP address management</span></span>

-   [<span data-ttu-id="1e4a6-171">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-171">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="1e4a6-172">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-172">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="1e4a6-173">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-173">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="1e4a6-174">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-174">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="1e4a6-175">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-175">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="1e4a6-176">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-176">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="1e4a6-177">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-177">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="1e4a6-178">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-178">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="1e4a6-179">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-179">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="1e4a6-180">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-180">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="1e4a6-181">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-181">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="1e4a6-182">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-182">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="1e4a6-183">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-183">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="1e4a6-184">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-184">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="1e4a6-185">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-185">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="1e4a6-186">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-186">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="1e4a6-187">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-187">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="1e4a6-188">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-188">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="1e4a6-189">Conversione della stringa di indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-189">IP address string conversion</span></span>

-   [<span data-ttu-id="1e4a6-190">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-190">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="1e4a6-191">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-191">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="1e4a6-192">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-192">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="1e4a6-193">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-193">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="1e4a6-194">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-194">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="1e4a6-195">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-195">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="1e4a6-196">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-196">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="1e4a6-197">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-197">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="1e4a6-198">Gestione degli indirizzi ip adiacenti</span><span class="sxs-lookup"><span data-stu-id="1e4a6-198">IP neighbor address management</span></span>

-   [<span data-ttu-id="1e4a6-199">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-199">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="1e4a6-200">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-200">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="1e4a6-201">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-201">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="1e4a6-202">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-202">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="1e4a6-203">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-203">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="1e4a6-204">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-204">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="1e4a6-205">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-205">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="1e4a6-206">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-206">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="1e4a6-207">Gestione dei percorsi IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-207">IP path management</span></span>

-   [<span data-ttu-id="1e4a6-208">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-208">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="1e4a6-209">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-209">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="1e4a6-210">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-210">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="1e4a6-211">Gestione delle route IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-211">IP route management</span></span>

-   [<span data-ttu-id="1e4a6-212">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-212">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="1e4a6-213">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-213">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="1e4a6-214">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-214">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="1e4a6-215">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-215">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="1e4a6-216">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-216">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="1e4a6-217">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-217">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="1e4a6-218">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-218">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="1e4a6-219">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-219">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="1e4a6-220">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-220">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="1e4a6-221">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-221">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="1e4a6-222">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-222">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="1e4a6-223">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-223">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="1e4a6-224">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-224">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="1e4a6-225">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-225">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="1e4a6-226">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-226">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="1e4a6-227">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-227">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="1e4a6-228">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-228">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="1e4a6-229">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-229">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="1e4a6-230">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-230">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="1e4a6-231">Gestione della memoria delle tabelle IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-231">IP table memory management</span></span>

-   [<span data-ttu-id="1e4a6-232">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-232">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="1e4a6-233">Utilità IP</span><span class="sxs-lookup"><span data-stu-id="1e4a6-233">IP utility</span></span>

-   [<span data-ttu-id="1e4a6-234">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-234">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="1e4a6-235">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-235">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="1e4a6-236">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-236">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="1e4a6-237">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-237">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="1e4a6-238">Configurazione di rete</span><span class="sxs-lookup"><span data-stu-id="1e4a6-238">Network configuration</span></span>

-   [<span data-ttu-id="1e4a6-239">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-239">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="1e4a6-240">Notifica</span><span class="sxs-lookup"><span data-stu-id="1e4a6-240">Notification</span></span>

-   [<span data-ttu-id="1e4a6-241">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-241">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="1e4a6-242">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-242">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="1e4a6-243">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-243">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="1e4a6-244">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-244">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="1e4a6-245">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-245">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="1e4a6-246">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-246">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="1e4a6-247">Timestamp dei pacchetti</span><span class="sxs-lookup"><span data-stu-id="1e4a6-247">Packet timestamping</span></span>

-   [<span data-ttu-id="1e4a6-248">**CaptureInterfaceHardwareCrossTimestamp**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-248">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="1e4a6-249">**GetInterfaceActiveTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-249">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="1e4a6-250">**GetInterfaceSupportedTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-250">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="1e4a6-251">**RegisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-251">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="1e4a6-252">**UnregisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-252">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="1e4a6-253">Prenotazione di porte persistenti</span><span class="sxs-lookup"><span data-stu-id="1e4a6-253">Persistent port reservation</span></span>

-   [<span data-ttu-id="1e4a6-254">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-254">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="1e4a6-255">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-255">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="1e4a6-256">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-256">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="1e4a6-257">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-257">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="1e4a6-258">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-258">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="1e4a6-259">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-259">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="1e4a6-260">Integrità della sicurezza</span><span class="sxs-lookup"><span data-stu-id="1e4a6-260">Security health</span></span>

-   <span data-ttu-id="1e4a6-261">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e4a6-261">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="1e4a6-262">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e4a6-262">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="1e4a6-263">Queste funzioni sono definite solo in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1e4a6-263">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="1e4a6-264">Queste funzioni non sono disponibili in Windows Vista, né in Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1e4a6-264">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="1e4a6-265">Teredo Gestione client IPv6</span><span class="sxs-lookup"><span data-stu-id="1e4a6-265">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="1e4a6-266">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-266">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="1e4a6-267">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-267">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="1e4a6-268">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-268">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="1e4a6-269">Transmission Control Protocol (TCP) e UDP (User Datagram Protocol)</span><span class="sxs-lookup"><span data-stu-id="1e4a6-269">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="1e4a6-270">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-270">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="1e4a6-271">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-271">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="1e4a6-272">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-272">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="1e4a6-273">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-273">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="1e4a6-274">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-274">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="1e4a6-275">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-275">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="1e4a6-276">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-276">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="1e4a6-277">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-277">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="1e4a6-278">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-278">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="1e4a6-279">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-279">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="1e4a6-280">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-280">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="1e4a6-281">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-281">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="1e4a6-282">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-282">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="1e4a6-283">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-283">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="1e4a6-284">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-284">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="1e4a6-285">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-285">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="1e4a6-286">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-286">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="1e4a6-287">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-287">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="1e4a6-288">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-288">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="1e4a6-289">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-289">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="1e4a6-290">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-290">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="1e4a6-291">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-291">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="1e4a6-292">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-292">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="1e4a6-293">API deprecate</span><span class="sxs-lookup"><span data-stu-id="1e4a6-293">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="1e4a6-294">Queste funzioni sono deprecate e non sono supportate da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4a6-294">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="1e4a6-295">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-295">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="1e4a6-296">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="1e4a6-296">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
