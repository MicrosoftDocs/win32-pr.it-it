---
description: I comandi Netsh per IPv6 forniscono uno strumento da riga di comando che è possibile utilizzare per eseguire query e configurare interfacce, indirizzi, cache e route IPv6. I comandi netsh interface IPv6 sono supportati in Windows XP con Service Pack 1 (SP1) e versioni successive.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129146"
---
# <a name="netshexe"></a><span data-ttu-id="d85e8-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="d85e8-104">Netsh.exe</span></span>

<span data-ttu-id="d85e8-105">I comandi Netsh per IPv6 forniscono uno strumento da riga di comando che è possibile utilizzare per eseguire query e configurare interfacce, indirizzi, cache e route IPv6.</span><span class="sxs-lookup"><span data-stu-id="d85e8-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="d85e8-106">I comandi netsh interface IPv6 sono supportati in Windows XP con Service Pack 1 (SP1) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d85e8-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="d85e8-107">Netsh.exe dispone di molti sottocomandi per IPv6.</span><span class="sxs-lookup"><span data-stu-id="d85e8-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="d85e8-108">Un elenco completo di opzioni per netsh interface IPv6 è disponibile dal prompt dei comandi in Windows XP con SP1 e versioni successive digitando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d85e8-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="d85e8-109">**netsh interface IPv6/?**</span><span class="sxs-lookup"><span data-stu-id="d85e8-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="d85e8-110">La documentazione su tutti i comandi **netsh** per IPv6 è disponibile anche in linea su TechNet.</span><span class="sxs-lookup"><span data-stu-id="d85e8-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="d85e8-111">Per ulteriori informazioni su **netsh** in Windows Server 2008, vedere [comandi Netsh per l'interfaccia (IPv4 e IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d85e8-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="d85e8-112">Per ulteriori informazioni su **netsh** in Windows Server 2003, vedere [comandi Netsh per l'interfaccia IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d85e8-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="d85e8-113">Di seguito sono riportati alcuni comandi di uso comune per IPv6, sebbene siano supportati molti altri comandi:</span><span class="sxs-lookup"><span data-stu-id="d85e8-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="d85e8-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span><span class="sxs-lookup"><span data-stu-id="d85e8-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-115">Aggiunge un indirizzo IPv6 a un'interfaccia specifica nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="d85e8-116">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface IPv6 Add DNS**</span><span class="sxs-lookup"><span data-stu-id="d85e8-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-118">Aggiunge un indirizzo IPv6 del server DNS all'elenco di server DNS configurati in modo statico per l'interfaccia specificata nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="d85e8-119">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span><span class="sxs-lookup"><span data-stu-id="d85e8-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-121">Aggiunge una route per un indirizzo di prefisso IPv6 specificato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="d85e8-122">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span><span class="sxs-lookup"><span data-stu-id="d85e8-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-124">Elimina l'indirizzo IPv6 specificato da un'interfaccia specifica nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="d85e8-125">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**</span><span class="sxs-lookup"><span data-stu-id="d85e8-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-127">Elimina un indirizzo del server DNS dall'elenco di server DNS configurati in modo statico per l'interfaccia specificata nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="d85e8-128">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**interfaccia netsh interface ipv6 delete**</span><span class="sxs-lookup"><span data-stu-id="d85e8-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-130">Elimina un'interfaccia specificata dallo stack IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="d85e8-131">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span><span class="sxs-lookup"><span data-stu-id="d85e8-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-133">Elimina una route per un indirizzo di prefisso IPv6 specificato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="d85e8-134">Questo comando contiene parametri di sottoopzione che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="d85e8-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**dump IPv6 interfaccia netsh**</span><span class="sxs-lookup"><span data-stu-id="d85e8-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-136">Crea uno script che contiene i comandi per creare la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="d85e8-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="d85e8-137">Se viene salvato in un file, lo script può essere usato per ripristinare le impostazioni di configurazione modificate.</span><span class="sxs-lookup"><span data-stu-id="d85e8-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span><span class="sxs-lookup"><span data-stu-id="d85e8-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-139">Installa il protocollo IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span><span class="sxs-lookup"><span data-stu-id="d85e8-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-141">Riavvia le interfacce IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface IPv6 reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="d85e8-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-143">Reimposta lo stato di configurazione IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span><span class="sxs-lookup"><span data-stu-id="d85e8-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-145">Consente di visualizzare i parametri di configurazione globali per IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface IPv6 Mostra indirizzo**</span><span class="sxs-lookup"><span data-stu-id="d85e8-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-147">Visualizza tutti gli indirizzi IPv6 o tutti gli indirizzi IPv6 in un'interfaccia specifica nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="d85e8-148">Questo comando contiene parametri di sottoopzione che potrebbero essere necessari.</span><span class="sxs-lookup"><span data-stu-id="d85e8-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d85e8-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span><span class="sxs-lookup"><span data-stu-id="d85e8-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="d85e8-150">Disinstalla il protocollo IPv6 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d85e8-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="d85e8-151">Comandi Netsh per IPv4</span><span class="sxs-lookup"><span data-stu-id="d85e8-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="d85e8-152">Sono disponibili comandi netsh simili per IPv4.</span><span class="sxs-lookup"><span data-stu-id="d85e8-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="d85e8-153">Un elenco completo di opzioni per i comandi netsh da usare con IPv4 è disponibile dal prompt dei comandi in Windows XP con SP1 e versioni successive digitando quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d85e8-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="d85e8-154">**netsh interface IP/?**</span><span class="sxs-lookup"><span data-stu-id="d85e8-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="d85e8-155">La documentazione su tutti i comandi Netsh per IPv4 è disponibile anche in linea su TechNet.</span><span class="sxs-lookup"><span data-stu-id="d85e8-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="d85e8-156">Per ulteriori informazioni, vedere [comandi Netsh per l'interfaccia IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="d85e8-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
