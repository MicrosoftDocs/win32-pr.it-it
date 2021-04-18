---
description: Uso di COPP (Certified Output Protocol)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Uso di COPP (Certified Output Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314398"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Uso di COPP (Certified Output Protocol)

Certified Output Protection Protocol (COPP) consente a un'applicazione di proteggere un flusso video mentre passa dalla scheda grafica al dispositivo di visualizzazione. Un'applicazione può usare COPP per individuare il tipo di connettore fisico collegato al dispositivo di visualizzazione e i tipi di protezione dell'output disponibili. Tra i meccanismi di protezione sono inclusi i seguenti:

-   High-Bandwidth protezione del contenuto digitali (HDCP)
-   Sistema di gestione della generazione di copia: analogico (CGMS-A)
-   Protezione copia analogica (ACP)

Se la scheda grafica supporta uno di questi meccanismi, l'applicazione può utilizzare COPP per impostare il livello di protezione.

COPP definisce un protocollo usato per stabilire un canale di comunicazione sicuro con il driver di grafica. USA i codici Mac (Message Authentication Code) per verificare l'integrità dei comandi COPP passati tra l'applicazione e il driver di visualizzazione. L'applicazione usa COPP chiamando i metodi sull'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) del filtro renderer video mixing (VMR-7 o VMR-9).

COPP non definisce informazioni sui criteri per i diritti digitali che possono essere applicati al contenuto multimediale digitale. Inoltre, COPP non implementa alcun sistema di protezione dell'output. Il protocollo COPP fornisce semplicemente un modo per impostare ed eseguire query sui livelli di protezione sulla scheda grafica, usando i sistemi di protezione forniti dall'adapter.

In questa sezione si presuppone che l'utente abbia familiarità con le tecnologie seguenti:

-   DirectShow
-   Windows Media Format SDK
-   XML
-   Crittografia a chiave pubblica e crittografia simmetrica

Negli esempi di codice di questa sezione viene utilizzato CryptoAPI di Microsoft per eseguire operazioni di crittografia. Questa sezione contiene i seguenti argomenti:

-   [Panoramica di COPP](overview-of-copp.md)
-   [Recupero della catena di certificati del driver](obtaining-the-drivers-certificate-chain.md)
-   [Convalida della catena di certificati](validating-the-certificate-chain.md)
-   [Elenchi di revoche dei certificati](certificate-revocation-lists.md)
-   [Importazione della chiave pubblica del driver](importing-the-drivers-public-key.md)
-   [Avvio di una sessione COPP](initiating-a-copp-session.md)
-   [Invio di richieste di stato di COPP](sending-copp-status-requests.md)
-   [Invio di comandi COPP](sending-copp-commands.md)
-   [Verifica se un driver di grafica supporta COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [Riferimento alla query COPP](copp-query-reference.md)
-   [Riferimento al comando COPP](copp-command-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del renderer video mixing](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



