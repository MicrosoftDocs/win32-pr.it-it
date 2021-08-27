---
description: Internet Protocol Suite è il protocollo di rete dominante usato nelle reti aziendali e in Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Supporto del protocollo di rete Winsock in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309b476669d7e27513c3e89acfbed135d425b234ccdf28a89ad74680a8cb596c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097691"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Supporto del protocollo di rete Winsock in Windows

Internet Protocol Suite è il protocollo di rete dominante usato nelle reti aziendali e in Internet. Internet Protocol Suite rappresenta un'ampia raccolta di protocolli di rete a più livelli. Internet Protocol Suite viene spesso definito TCP/IP in base a due dei protocolli più importanti inclusi nella suite: il protocollo IP (Internet Protocol) e il Transmission Control Protocol (TCP).

IPv6 e IPv4 rappresentano le due versioni disponibili del protocollo Internet. TCP è uno dei diversi importanti servizi di rete spesso definiti protocolli IP che operano su reti IPv6 e IPv4. Il protocollo UDP (User Datagram Protocol) e Internet Control Message Protocol (ICMP) sono altri protocolli IP importanti usati sulle reti IPv6 e IPv4. Esistono diversi altri protocolli IP che possono essere usati su reti IPv6 e IPv4.

Windows Sockets considera ogni suite di protocolli di rete come una famiglia di indirizzi univoca. Il protocollo IPv6 è quindi considerato la famiglia di indirizzi **AF \_ INET6** e il protocollo IPv4 è considerato la famiglia di indirizzi **AF \_ INET.** I protocolli IPv6 e IPv4 supportano l'uso di vari protocolli IP a più livelli, ad esempio TCP, UDP e ICMP.

Windows I socket sono stati inizialmente progettati per aggiungere il supporto per IPv4 Windows. Tuttavia, l'Windows di programmazione Sockets è stata progettata fin dall'inizio con la possibilità di supportare altre suite di protocolli di rete. Nel corso del tempo, le versioni di Windows e i socket Windows associati hanno incluso il supporto nativo per altre suite di protocolli di rete ,ad esempio IPX/SPX e AppleTalk. Il supporto per altri protocolli di rete era disponibile anche per le versioni di Windows software di terze parti dei fornitori.

Prima della crescita e della popolarità di Internet, sono stati usati diversi altri gruppi di protocolli di rete negli ambienti di rete, in particolare per le Intranet locali. La scelta di una suite di protocolli di rete è spesso basata sulle dimensioni della rete o sull'esperienza del personale di rete IT. Con la connettività Internet globale di oggi che collega anche le reti più piccole al resto del mondo, l'esperienza di rete in IPv6 e IPv4 è essenziale per i professionisti della rete. Di conseguenza, altre suite di protocolli di rete importanti in precedenza hanno ora un uso molto limitato e sono diventate obviate. Il supporto nativo per queste suite di protocolli di rete obviated, spesso definiti protocolli di rete legacy, è stato eliminato dalle versioni recenti di Microsoft Windows. Il supporto per alcuni di questi protocolli legacy può essere disponibile come software di terze parti dei fornitori (ad esempio ATM con hardware di rete ATM).

La tabella seguente identifica il supporto Windows per i gruppi di protocolli di rete comuni. 

| Protocollo di rete                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Non supportato (vedere Note)<br/> |
| IPv4<br/>                  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| NetBIOS (vedere Le note) <br/>  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| IrDA (vedere Note)<br/>      | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| Bluetooth (vedere Note)<br/> | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Non supportato<br/>             |
| IPX/SPX<br/>               | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| Appletalk<br/>             | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| Dlc<br/>                   | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Non supportato (vedere Note)<br/> | Non supportato (vedere Note)<br/> | Supportato<br/>                 |
| ATM<br/>                   | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato (vedere Note)<br/>     | Supportato (vedere Note)<br/>     | Supportato (vedere Note)<br/>     |
| Netbeui<br/>               | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Non supportato<br/>             | Non supportato<br/>             | Supportato (vedere le note)<br/>     |



 

**IPv6 in Windows 2000:** Il protocollo IPv6 è supportato in Windows 2000 con Service Pack 1 (SP1) e versioni successive con Microsoft IPv6 Technology Preview per Windows 2000.

**NetBIOS:** Il protocollo NetBIOS viene comunemente usato dai servizi di denominazione Windows. NetBIOS può usare più gruppi di protocolli di rete, tra cui IP (NetBIOS su TCP/IP), IPX/SPX e NetBEUI. Winsock supporta NetBIOS su TCP/IP (comunemente noto come NetBT) solo nelle versioni a 32 bit di Windows 7, Windows Server 2008 e Windows Vista. Winsock supporta NetBIOS su TCP/IP e NetBIOS usando IPX in Windows Server 2003 e Windows XP. Winsock supporta NetBIOS su TCP/IP, NetBIOS tramite IPX e NetBIOS tramite NetBEUI Windows 2000.

**IrDA:** Il Infrared Data Association (IrDA) è supportato se nel computer sono installati una porta a volta e un driver.

**Bluetooth:** Il supporto Winsock Bluetooth come suite di protocolli di rete include i profili PAN (Personal Area Network) e DUN (Dial up Networking) di Bluetooth. Bluetooth supporto in Windows include anche l'uso di Bluetooth Human Interface Device (HID) e di altri profili per la connessione a tastiere, dispositivi di puntamento e altri dispositivi di input non correlati ai protocolli di rete.

**DLC in Windows 2003 e Windows XP:** Il protocollo Data Link Control (DLC) è supportato in Windows Server 2003 e Windows XP quando è installato il driver DLC incluso in Microsoft Host Integration Server 2006, Host Integration Server 2004 o Host Integration Server 2000.

**ATM in Windows 2003, Windows XP e Windows 2000:** Il protocollo della modalità di trasferimento asincrono (ATM) è supportato in Windows Server 2003, Windows XP e Windows 2000 quando viene installata una scheda di rete ATM. Il protocollo per l'IP classico su ATM (talvolta abbreviato come CLIP/ATM) è definito in [RFC 2225](https://tools.ietf.org/html/rfc2225) e nei documenti correlati pubblicati da IETF. Windows Server 2003, Windows XP e Windows 2000 forniscono un'implementazione completa di questo standard.

**NetBEUI in Windows 2000:** Il protocollo NetBEUI non è supportato direttamente Windows socket. Tuttavia, il protocollo NetBIOS che può usare più protocolli di rete supporta l'uso del protocollo NetBEUI Windows 2000.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento tecnico per il servizio atm](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[IPv6 Technology Preview per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Irda](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Supporto di NDIS 5.0 e ATM in Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
