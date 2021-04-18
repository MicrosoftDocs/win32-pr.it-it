---
description: Internet Protocol Suite è il protocollo di rete dominante utilizzato nelle reti aziendali e in Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Supporto del protocollo di rete Winsock in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484925"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Supporto del protocollo di rete Winsock in Windows

Internet Protocol Suite è il protocollo di rete dominante utilizzato nelle reti aziendali e in Internet. Internet Protocol Suite rappresenta un'ampia raccolta di protocolli di rete sovrapposti. La suite di protocolli Internet è spesso definita TCP/IP in base a due dei protocolli più importanti inclusi nella suite, ovvero Internet Protocol (IP) e il Transmission Control Protocol (TCP).

IPv6 e IPv4 rappresentano le due versioni disponibili del protocollo Internet. TCP è uno dei numerosi servizi di rete importanti spesso indicati come protocolli IP che operano su reti IPv6 e IPv4. Il protocollo UDP (User Datagram Protocol) e il Internet Control Message Protocol (ICMP) sono altri protocolli IP importanti usati su reti IPv6 e IPv4. Sono disponibili diversi altri protocolli IP che possono essere usati su reti IPv6 e IPv4.

Windows Sockets considera ciascuna suite di protocolli di rete come famiglia di indirizzi univoca. Il protocollo IPv6 viene quindi considerato la famiglia di indirizzi **AF \_ INET6** e il protocollo IPv4 è considerato la famiglia di indirizzi **\_ inetti AF** . I protocolli IPv6 e IPv4 supportano l'utilizzo di diversi protocolli IP sovrapposti, ad esempio TCP, UDP e ICMP.

I socket di Windows sono stati inizialmente progettati per aggiungere il supporto per IPv4 a Windows. Tuttavia, l'interfaccia di programmazione Windows Sockets è stata progettata dall'inizio con la possibilità di supportare altri gruppi di protocolli di rete. Nel corso del tempo, le versioni di Windows e i socket Windows associati includono il supporto nativo per altre suite di protocolli di rete (ad esempio, IPX/SPX e AppleTalk). Il supporto per altri protocolli di rete è disponibile anche per le versioni di Windows come software di terze parti da fornitori.

Prima della crescita e della popolarità di Internet, diversi altri gruppi di protocolli di rete venivano usati in ambienti di rete, in particolare per le Intranet locali. La scelta di una suite di protocolli di rete è stata spesso basata sulla dimensione della rete o sulle competenze del personale IT. Con la connettività Internet globale odierna che collega anche le reti più piccole al resto del mondo, le competenze in rete in IPv6 e IPv4 sono essenziali per i professionisti della rete. Di conseguenza, altri gruppi di protocolli di rete precedentemente importanti sono ora in uso molto limitato e sono diventati ciecamente. Il supporto nativo per queste suite di protocolli di rete ciecamente, spesso denominate protocolli di rete legacy, è stato eliminato dalle versioni recenti di Microsoft Windows. Il supporto di alcuni di questi protocolli legacy potrebbe essere disponibile come software di terze parti da fornitori (ad esempio, ATM con hardware di rete ATM).

La tabella seguente identifica il supporto nativo di Windows per i gruppi di protocolli di rete comuni. 

| Protocollo di rete                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Non supportato (vedere le note)<br/> |
| IPv4<br/>                  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| NetBIOS (vedere le note) <br/>  | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| IrDA (vedere le note)<br/>      | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| Bluetooth (vedere le note)<br/> | Supportato<br/>     | Supportato<br/>     | Supportato<br/>     | Supportato<br/>                 | Supportato<br/>                 | Non supportato<br/>             |
| IPX/SPX<br/>               | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| AppleTalk<br/>             | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato<br/>                 | Supportato<br/>                 | Supportato<br/>                 |
| DLC<br/>                   | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Non supportato (vedere le note)<br/> | Non supportato (vedere le note)<br/> | Supportato<br/>                 |
| ATM<br/>                   | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Supportato (vedere le note)<br/>     | Supportato (vedere le note)<br/>     | Supportato (vedere le note)<br/>     |
| NetBEUI<br/>               | Non supportato<br/> | Non supportato<br/> | Non supportato<br/> | Non supportato<br/>             | Non supportato<br/>             | Supportato (vedere le note)<br/>     |



 

**IPv6 in Windows 2000:** Il protocollo IPv6 è supportato in Windows 2000 con Service Pack 1 (SP1) e versioni successive con Microsoft IPv6 Technology Preview per Windows 2000.

**NetBIOS:** Il protocollo NetBIOS viene comunemente usato per la denominazione dei servizi in Windows. NetBIOS può utilizzare più suite di protocolli di rete, tra cui IP (NetBIOS su TCP/IP), IPX/SPX e NetBEUI. Winsock supporta NetBIOS su TCP/IP (comunemente chiamata NetBT) solo nelle versioni a 32 bit di Windows 7, Windows Server 2008 e Windows Vista. Winsock supporta NetBIOS su TCP/IP e NetBIOS mediante IPX in Windows Server 2003 e Windows XP. Winsock supporta NetBIOS su TCP/IP, NetBIOS con IPX e NetBIOS con NetBEUI in Windows 2000.

**IrDA:** Il protocollo IrDA (Infrared Data Association) è supportato se il computer dispone di una porta e di un driver infrarossi installati.

**Bluetooth:** Il supporto Winsock per Bluetooth come gruppo di protocolli di rete include i profili di rete personale (PAN) Bluetooth e di connessione remota (DUN). Il supporto Bluetooth in Windows include anche l'uso del dispositivo HID (Human Interface Device) e di altri profili per la connessione a tastiere, dispositivi di puntamento e altri dispositivi di input che non sono correlati ai protocolli di rete.

**DLC in windows 2003 e Windows XP:** Il protocollo Data Link Control (DLC) è supportato in Windows Server 2003 e Windows XP quando il driver DLC incluso in Microsoft Host Integration Server 2006, Host Integration Server 2004 o Host Integration Server 2000 è installato.

**ATM in windows 2003, Windows XP e windows 2000:** Il protocollo ATM (Asynchronous Transfer Mode) è supportato in Windows Server 2003, Windows XP e Windows 2000 quando è installata una scheda di rete ATM. Il protocollo per l'IP classico su ATM (talvolta abbreviato come CLIP/ATM) è definito in [RFC 2225](https://tools.ietf.org/html/rfc2225) e nei documenti correlati pubblicati da IETF. Windows Server 2003, Windows XP e Windows 2000 forniscono un'implementazione completa di questo standard.

**NetBEUI in Windows 2000:** Il protocollo NetBEUI non è supportato direttamente da Windows Sockets. Tuttavia, il protocollo NetBIOS che può utilizzare più protocolli di rete supporta l'utilizzo del protocollo NetBEUI in Windows 2000.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento tecnico per ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[Anteprima della tecnologia IPv6 per Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[IrDA](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Supporto di NDIS 5,0 e ATM in Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
