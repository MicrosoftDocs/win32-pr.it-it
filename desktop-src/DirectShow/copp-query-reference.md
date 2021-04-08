---
description: Riferimento alla query COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Riferimento alla query COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049061"
---
# <a name="copp-query-reference"></a>Riferimento alla query COPP

In questa sezione vengono descritte le query di stato supportate da Certified Output Protocol (COPP). Per ogni query, viene elencato il GUID che definisce la query insieme ai dati di input e ai dati restituiti.



| Query                   | GUID                                     |
|-------------------------|------------------------------------------|
| Dati bus                | **\_COPPQUERYBUSDATA DXVA**               |
| Tipo connettore          | **\_COPPQUERYCONNECTORTYPE DXVA**         |
| Visualizza dati            | **\_COPPQUERYDISPLAYDATA DXVA**           |
| Dati chiave HDCP           | **\_COPPQUERYHDCPKEYDATA DXVA**           |
| Livello di protezione globale | **\_COPPQUERYGLOBALPROTECTIONLEVEL DXVA** |
| Livello di protezione locale  | **\_COPPQUERYLOCALPROTECTIONLEVEL DXVA**  |
| Tipo di protezione         | **\_COPPQUERYPROTECTIONTYPE DXVA**        |
| Signaling               | **\_COPPQUERYSIGNALING DXVA**             |



 

Query sui dati del bus

Restituisce il tipo di bus di I/O utilizzato dalla scheda grafica.

-   **GUID**: DXVA \_ COPPQueryBusData
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Il tipo di bus viene restituito nel membro **dwData** come flag dell'enumerazione [**\_ BusType di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .

Query tipo connettore

Restituisce il tipo di connettore fisico.

-   **GUID**: DXVA \_ COPPQueryConnectorType
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Il tipo di connettore viene restituito nel membro **dwData** come flag dell'enumerazione [**\_ ConnectorType di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .

Query dei dati di visualizzazione

Restituisce una descrizione del segnale video trasmesso sul connettore.

Il segnale video trasmesso sul connettore non ha necessariamente lo stesso formato della modalità di visualizzazione del desktop. Ad esempio, la modalità di visualizzazione del desktop può essere 1024x768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-video che trasmette un segnale video a 720x480 pixel, 60/1.01 Hz interlacciato. In tal caso, il driver restituirà la risoluzione del segnale S-video, non la risoluzione del desktop.

-   **GUID**: DXVA \_ COPPQueryDisplayData
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusDisplayData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .

Query sui dati della chiave HDCP

Restituisce il vettore di selezione della chiave HDCP del dispositivo (B-KSV).

KSV è un identificatore fornito al produttore del dispositivo e viene usato nel processo di autenticazione e configurazione di HDCP. L'applicazione deve controllare questo valore rispetto all'elenco di KSVs revocati. Il meccanismo per ottenere l'elenco di revoche KSV non rientra nell'ambito del protocollo COPP. Per ulteriori informazioni, consultare la specifica HDCP.

Questa query determina anche se il dispositivo HDCP connesso è un monitor o un ripetitore HDCP. L'applicazione non deve riprodurre contenuti protetti se il dispositivo HDCP è un ripetitore HDCP, perché questi non sono supportati da COPP.

-   **GUID**: DXVA \_ COPPQueryHDCPKeyData
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusHDCPKeyData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .

Query livello di protezione globale

Restituisce il livello di protezione globale per un meccanismo di protezione specificato.

Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui il driver di grafica ha richiesto di applicare la protezione. Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la funzione **ChangeDisplaySettingsEx** . In tal caso, il livello di protezione globale rifletterebbe questa impostazione, anche se non è stata richiesta tramite COPP.

-   **GUID**: DXVA \_ COPPQueryGlobalProtectionLevel
-   **Dati di input**: meccanismo di protezione per la query, specificato come intero a 32 bit. Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md).
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Il livello di protezione corrente viene restituito nel membro **dwData** . Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore del membro **dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.

    | Meccanismo di protezione | Enumerazione                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**\_Livello di \_ protezione \_ ACP Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Livello di \_ protezione \_ CGMSA di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | PROTOCOLLO HDCP                 | [**\_Livello di \_ protezione Copp HDCP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Query livello di protezione locale

Restituisce il livello di protezione locale per un meccanismo di protezione specificato.

Il livello di protezione locale è il livello di protezione richiesto tramite la sessione COPP corrente. Il driver potrebbe impostare un livello di protezione superiore.

-   **GUID**: DXVA \_ COPPQueryLocalProtectionLevel
-   **Dati di input**: meccanismo di protezione per la query, come intero a 32 bit. Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md).
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Il livello di protezione corrente viene restituito nel membro **dwData** . Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore del membro **dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.

    | Meccanismo di protezione | Enumerazione                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**\_Livello di \_ protezione \_ ACP Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Livello di \_ protezione \_ CGMSA di Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | PROTOCOLLO HDCP                 | [**\_Livello di \_ protezione Copp HDCP \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Query del tipo di protezione

Restituisce i meccanismi di protezione disponibili per il connettore.

-   **GUID**: DXVA \_ COPPQueryProtectionType
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . I meccanismi di protezione vengono restituiti nel membro **dwData** come una combinazione di zero o più flag. Vedere [flag del tipo di protezione Copp](copp-protection-type-flags.md). Se è disponibile più di un meccanismo di protezione, i flag vengono combinati con un **or** bit per bit.

Query di segnalazione

Restituisce un elenco di tutti gli standard di protezione supportati dal driver, lo standard attualmente attivo e le proporzioni correnti o altri dati di segnalazione.

-   **GUID**: DXVA \_ COPPQuerySignaling
-   **Dati di input**: nessuno.
-   **Dati restituiti**: restituisce una [**struttura \_ COPPStatusSignalingCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



