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
# <a name="netshexe"></a>Netsh.exe

I comandi Netsh per IPv6 forniscono uno strumento da riga di comando che è possibile utilizzare per eseguire query e configurare interfacce, indirizzi, cache e route IPv6. I comandi netsh interface IPv6 sono supportati in Windows XP con Service Pack 1 (SP1) e versioni successive.

Netsh.exe dispone di molti sottocomandi per IPv6. Un elenco completo di opzioni per netsh interface IPv6 è disponibile dal prompt dei comandi in Windows XP con SP1 e versioni successive digitando quanto segue:

**netsh interface IPv6/?**

La documentazione su tutti i comandi **netsh** per IPv6 è disponibile anche in linea su TechNet. Per ulteriori informazioni su **netsh** in Windows Server 2008, vedere [comandi Netsh per l'interfaccia (IPv4 e IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)). Per ulteriori informazioni su **netsh** in Windows Server 2003, vedere [comandi Netsh per l'interfaccia IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).

Di seguito sono riportati alcuni comandi di uso comune per IPv6, sebbene siano supportati molti altri comandi:

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**
</dt> <dd>

Aggiunge un indirizzo IPv6 a un'interfaccia specifica nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface IPv6 Add DNS**
</dt> <dd>

Aggiunge un indirizzo IPv6 del server DNS all'elenco di server DNS configurati in modo statico per l'interfaccia specificata nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**
</dt> <dd>

Aggiunge una route per un indirizzo di prefisso IPv6 specificato nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**
</dt> <dd>

Elimina l'indirizzo IPv6 specificato da un'interfaccia specifica nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**
</dt> <dd>

Elimina un indirizzo del server DNS dall'elenco di server DNS configurati in modo statico per l'interfaccia specificata nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**interfaccia netsh interface ipv6 delete**
</dt> <dd>

Elimina un'interfaccia specificata dallo stack IPv6 nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**
</dt> <dd>

Elimina una route per un indirizzo di prefisso IPv6 specificato nel computer locale. Questo comando contiene parametri di sottoopzione che è necessario specificare.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**dump IPv6 interfaccia netsh**
</dt> <dd>

Crea uno script che contiene i comandi per creare la configurazione corrente. Se viene salvato in un file, lo script può essere usato per ripristinare le impostazioni di configurazione modificate.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**
</dt> <dd>

Installa il protocollo IPv6 nel computer locale.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**
</dt> <dd>

Riavvia le interfacce IPv6 nel computer locale.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface IPv6 reimpostazione**
</dt> <dd>

Reimposta lo stato di configurazione IPv6 nel computer locale.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**
</dt> <dd>

Consente di visualizzare i parametri di configurazione globali per IPv6 nel computer locale.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface IPv6 Mostra indirizzo**
</dt> <dd>

Visualizza tutti gli indirizzi IPv6 o tutti gli indirizzi IPv6 in un'interfaccia specifica nel computer locale. Questo comando contiene parametri di sottoopzione che potrebbero essere necessari.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**
</dt> <dd>

Disinstalla il protocollo IPv6 nel computer locale.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Comandi Netsh per IPv4

Sono disponibili comandi netsh simili per IPv4. Un elenco completo di opzioni per i comandi netsh da usare con IPv4 è disponibile dal prompt dei comandi in Windows XP con SP1 e versioni successive digitando quanto segue:

**netsh interface IP/?**

La documentazione su tutti i comandi Netsh per IPv4 è disponibile anche in linea su TechNet. Per ulteriori informazioni, vedere [comandi Netsh per l'interfaccia IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))

 

 
