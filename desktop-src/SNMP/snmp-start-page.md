---
title: Servizio SNMP
description: L'implementazione di Microsoft Windows del Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni della rete, controllare l'utilizzo della rete e rilevare errori di rete o accedere in modo non appropriato. Importante l'API Microsoft Windows SNMP supporta solo le versioni di protocollo fino a SNMPv2C. Non supporta versioni successive del protocollo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047241"
---
# <a name="snmp-service"></a>Servizio SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

## <a name="purpose"></a>Scopo

L'implementazione di Microsoft Windows del Simple Network Management Protocol (SNMP) viene usata per configurare i dispositivi remoti, monitorare le prestazioni della rete, controllare l'utilizzo della rete e rilevare errori di rete o accedere in modo non appropriato.

> [!IMPORTANT]
> L'API Microsoft Windows SNMP supporta solo le versioni di protocollo fino a SNMPv2C. Non supporta versioni successive del protocollo.

 

## <a name="where-applicable"></a>Se applicabile

SNMP utilizza un'architettura distribuita costituita da applicazioni di gestione e applicazioni agente. Il servizio SNMP implementa un agente SNMP. Per utilizzare le informazioni fornite dal servizio SNMP, è necessario disporre di almeno un host in cui sia in esecuzione un'applicazione di gestione SNMP. È possibile utilizzare software di gestione SNMP di terze parti oppure sviluppare un'applicazione software di gestione SNMP personalizzata. A questo scopo sono disponibili le API seguenti:

-   API di gestione SNMP, un set di funzioni che è possibile utilizzare per sviluppare rapidamente sistemi di gestione SNMP di base
-   API WinSNMP, versione 2,0, un set di funzioni per la codifica, la decodifica, l'invio e la ricezione di messaggi SNMP

Inoltre, l'API dell'agente di estensione SNMP definisce l'interfaccia tra il servizio SNMP e le DLL dell'agente di estensione SNMP di terze parti. È possibile utilizzare le funzioni API dell'utilità SNMP per semplificare l'elaborazione dei messaggi SNMP.

## <a name="developer-audience"></a>Sviluppatori

Le API elencate nella sezione precedente sono progettate per l'uso da parte dei programmatori C/C++. Sono necessari familiarità con SNMP e SNMPv2C, nonché una conoscenza pratica dei concetti di rete e di gestione della rete.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per ulteriori informazioni sul sistema operativo necessario per utilizzare una particolare funzione, vedere la sezione requisiti della pagina di riferimento per tale funzione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità in SNMP](new-in-snmp.md)<br/>                                                            | Informazioni sugli aggiornamenti di SNMP.<br/>                                                                                                      |
| [Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | Informazioni di riferimento sulle API per SNMP, tra cui l'API di gestione SNMP, l'API dell'agente di estensione SNMP e le funzioni API dell'utilità SNMP.<br/> |
| [API WinSNMP](snmp-reference.md)<br/>                                                         | Informazioni di riferimento sulle API per Microsoft Windows SNMP Application Programming Interface (API WinSNMP). <br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dynamic Host Configuration Protocol (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Gestione della rete](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Routing and Remote Access Service](/windows/desktop/RRAS/portal)
</dt> </dl>

 

