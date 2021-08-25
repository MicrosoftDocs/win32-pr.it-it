---
description: Informazioni di riferimento sulla query COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Informazioni di riferimento sulla query COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d36cde152600faaa1dd567faac916bfa8281e2b2edb9464074fe34a58d5011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909661"
---
# <a name="copp-query-reference"></a>Informazioni di riferimento sulla query COPP

Questa sezione descrive le query sullo stato supportate dal protocollo COPP (Certified Output Protection Protocol). Per ogni query viene elencato il GUID che definisce la query, insieme ai dati di input e ai dati restituiti.



| Query                   | GUID                                     |
|-------------------------|------------------------------------------|
| Dati bus                | **DXVA \_ COPPQueryBusData**               |
| Tipo connettore          | **DXVA \_ COPPQueryConnectorType**         |
| Visualizzare i dati            | **DXVA \_ COPPQueryDisplayData**           |
| Dati della chiave HDCP           | **DXVA \_ COPPQueryHDCPKeyData**           |
| Livello di protezione globale | **DXVA \_ COPPQueryGlobalProtectionLevel** |
| Livello di protezione locale  | **DXVA \_ COPPQueryLocalProtectionLevel**  |
| Tipo di protezione         | **DXVA \_ COPPQueryProtectionType**        |
| Signaling               | **DXVA \_ COPPQuerySignaling**             |



 

Query sui dati del bus

Restituisce il tipo di bus di I/O utilizzato dalla scheda grafica.

-   **GUID:** DXVA \_ COPPQueryBusData
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Il tipo di bus viene restituito nel **membro dwData** come flag dall'enumerazione [**\_ CoPP BusType.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype)

Query sul tipo di connettore

Restituisce il tipo di connettore fisico.

-   **GUID:** DXVA \_ COPPQueryConnectorType
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Il tipo di connettore viene restituito nel **membro dwData** come flag dall'enumerazione [**\_ COPP ConnectorType.**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype)

Visualizzare la query sui dati

Restituisce una descrizione del segnale video trasmesso tramite il connettore.

Il segnale video trasmesso tramite il connettore non ha necessariamente lo stesso formato della modalità di visualizzazione desktop. Ad esempio, la modalità di visualizzazione desktop potrebbe essere di 1024x768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-Video che trasmette un segnale video a 720x480 pixel, 60/1,01 Hz interlacciato. In tal caso, il driver restituirebbe la risoluzione del segnale S-Video, non la risoluzione desktop.

-   **GUID:** DXVA \_ COPPQueryDisplayData
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusDisplayData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata)

Query sui dati della chiave HDCP

Restituisce il vettore di selezione della chiave HDCP (B-KSV) del dispositivo.

Il KSV è un identificatore fornito al produttore del dispositivo e viene usato nel processo di autenticazione e configurazione HDCP. L'applicazione deve controllare questo valore rispetto all'elenco di KSV revocati. Il meccanismo per ottenere l'elenco di revoche KSV non rientra nell'ambito del protocollo COPP. Per altre informazioni, vedere la specifica HDCP.

Questa query determina anche se il dispositivo HDCP connesso è un monitor o un ripetitore HDCP. L'applicazione non deve riprodurre contenuto protetto se il dispositivo HDCP è un ripetitore HDCP, perché non sono supportati da COPP.

-   **GUID:** DXVA \_ COPPQueryHDCPKeyData
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusHDCPKeyData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata)

Query a livello di protezione globale

Restituisce il livello di protezione globale per un meccanismo di protezione specificato.

Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui è stato richiesto al driver di grafica di applicare la protezione. Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la **funzione ChangeDisplaySettingsEx.** In tal caso, il livello di protezione globale riflette questa impostazione, anche se non è stata richiesta tramite COPP.

-   **GUID:** DXVA \_ COPPQueryGlobalProtectionLevel
-   **Dati di input:** meccanismo di protezione per l'esecuzione di query, specificato come intero a 32 bit. Vedere [Flag dei tipi di protezione COPP.](copp-protection-type-flags.md)
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Il livello di protezione corrente viene restituito nel **membro dwData.** Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore del **membro dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.

    | Meccanismo di protezione | Enumerazione                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Livello di protezione \_ copp ACP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Livello di \_ protezione COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Livello di protezione \_ HDCP COPP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Query a livello di protezione locale

Restituisce il livello di protezione locale per un meccanismo di protezione specificato.

Il livello di protezione locale è il livello di protezione richiesto tramite la sessione COPP corrente. Il driver potrebbe impostare un livello di protezione superiore.

-   **GUID:** DXVA \_ COPPQueryLocalProtectionLevel
-   **Dati di input:** meccanismo di protezione per l'esecuzione di query, come intero a 32 bit. Vedere [Flag dei tipi di protezione COPP.](copp-protection-type-flags.md)
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) Il livello di protezione corrente viene restituito nel **membro dwData.** Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query. Per ogni meccanismo di protezione, il valore del **membro dwData** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.

    | Meccanismo di protezione | Enumerazione                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Livello di protezione \_ copp ACP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**Livello di \_ protezione COPP CGMSA \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**Livello di protezione \_ HDCP COPP \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Query sul tipo di protezione

Restituisce i meccanismi di protezione disponibili per il connettore.

-   **GUID:** DXVA \_ COPPQueryProtectionType
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) I meccanismi di protezione vengono restituiti nel **membro dwData** come combinazione di zero o più flag. Vedere [Flag dei tipi di protezione COPP.](copp-protection-type-flags.md) Se sono disponibili più meccanismi di protezione, i flag vengono combinati con or bit per **bit.**

Query di segnalazione

Restituisce un elenco di tutti gli standard di protezione supportati dal driver, lo standard attualmente attivo e le proporzioni correnti o altri dati di segnalazione.

-   **GUID:** DXVA \_ COPPQuerySignaling
-   **Dati di input:** nessuno.
-   **Dati restituiti:** restituisce [**una struttura \_ DXVA COPPStatusSignalingCmdData.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



