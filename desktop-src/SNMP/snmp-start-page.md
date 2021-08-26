---
title: Servizio SNMP
description: L'implementazione microsoft Windows di Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni di rete, controllare l'utilizzo della rete e rilevare errori di rete o accessi inappropriati. Importante L'API SNMP di Microsoft Windows supporta solo le versioni del protocollo fino a SNMPv2C. Non supporta le versioni successive del protocollo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dfb56450edbb6d5f18daa635e30e08e5914eb48fefb28013a66276dbc9a0a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886391"
---
# <a name="snmp-service"></a>Servizio SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

## <a name="purpose"></a>Scopo

L'implementazione microsoft Windows di Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni di rete, controllare l'utilizzo della rete e rilevare errori di rete o accessi inappropriati.

> [!IMPORTANT]
> L'API SNMP di Microsoft Windows supporta solo le versioni del protocollo fino a SNMPv2C. Non supporta le versioni successive del protocollo.

 

## <a name="where-applicable"></a>Se applicabile

SNMP usa un'architettura distribuita costituita da applicazioni di gestione e applicazioni agente. Il servizio SNMP implementa un agente SNMP. Per usare le informazioni fornite dal servizio SNMP, è necessario disporre di almeno un host che esegue un'applicazione di gestione SNMP. È possibile usare software di gestione SNMP di terze parti oppure sviluppare un'applicazione software di gestione SNMP. A questo scopo sono disponibili le API seguenti:

-   SNMP API Gestione, un set di funzioni che possono essere usate per sviluppare rapidamente sistemi di gestione SNMP di base
-   API WinSNMP, versione 2.0, un set di funzioni per la codifica, la decodifica, l'invio e la ricezione di messaggi SNMP

Inoltre, l'API dell'agente di estensione SNMP definisce l'interfaccia tra il servizio SNMP e le DLL dell'agente di estensione SNMP di terze parti. Le funzioni api dell'utilità SNMP possono essere usate per semplificare l'elaborazione dei messaggi SNMP.

## <a name="developer-audience"></a>Sviluppatori

Le API elencate nella sezione precedente sono progettate per l'uso da parte dei programmatori C/C++. È necessaria una certa familiarità con SNMP e SNMPv2C, nonché una conoscenza approfondita dei concetti relativi alla rete e alla gestione della rete.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per altre informazioni sul sistema operativo necessario per usare una funzione specifica, vedere la sezione Requisiti della pagina di riferimento per tale funzione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità di SNMP](new-in-snmp.md)<br/>                                                            | Informazioni sugli aggiornamenti di SNMP.<br/>                                                                                                      |
| [Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | Informazioni e informazioni di riferimento sulle API per SNMP, incluse le funzioni SNMP API Gestione, SNMP Extension Agent API e SNMP Utility API.<br/> |
| [WinSNMP API](snmp-reference.md)<br/>                                                         | Informazioni e informazioni di riferimento sulle API per Microsoft Windows SNMP Application Programming Interface (API WinSNMP). <br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Gestione della rete](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Routing and Remote Access Service](/windows/desktop/RRAS/portal)
</dt> </dl>

 

