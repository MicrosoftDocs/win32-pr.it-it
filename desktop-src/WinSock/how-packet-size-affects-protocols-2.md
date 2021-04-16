---
description: I problemi relativi alle dimensioni dei pacchetti multimediali descritti nell'argomento relativo alle dimensioni dei pacchetti multimediali influiscono sui diversi \_ protocolli IPX PF in modo diverso.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Impatto delle dimensioni del pacchetto sui protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343506"
---
# <a name="how-packet-size-affects-protocols"></a>Impatto delle dimensioni del pacchetto sui protocolli

I problemi relativi alle dimensioni dei pacchetti multimediali descritti nell'argomento [relativo alle dimensioni dei pacchetti multimediali](about-media-packet-size-2.md)influiscono sui diversi \_ protocolli IPX PF in modo diverso. Una strategia comune per la gestione di diversi vincoli di dimensioni del router e dei supporti consiste nell'usare le dimensioni massime dei supporti quando il numero di rete della stazione remota corrisponde alla stazione locale ed eseguire il fallback alla dimensione minima del pacchetto in caso contrario.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

Fornisce un servizio datagramma; ogni datagramma deve risiedere entro la dimensione massima del pacchetto. Winsock imposta la dimensione massima del pacchetto del datagramma sulle dimensioni del pacchetto multimediale locale meno l'intestazione IPX. Tenere presente, tuttavia, che se il pacchetto viene indirizzato, è possibile che si verifichino restrizioni del router in Route. Assicurarsi che l'applicazione sia in grado di eseguire il fallback a datagrammi a 546 byte.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>\_SPX NSPROTO
</dt> <dd>

Fornisce servizi per pacchetti di flusso e sequenziato. Winsock IPX/SPX consente ai flussi di dati e ai messaggi di estendersi su più pacchetti, pertanto le dimensioni dei pacchetti non limitano la quantità di dati gestiti da [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv). Tuttavia, le dimensioni dei supporti sottostanti devono essere impostate correttamente oppure il primo pacchetto di grandi dimensioni sarà non recapitabile e la connessione verrà reimpostata. Se la stazione di destinazione si trova nella rete locale, Winsock imposta le dimensioni del pacchetto sulle dimensioni del pacchetto multimediale. In caso contrario, il valore predefinito è 512 byte. Queste dimensioni possono essere modificate immediatamente dopo la [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o l' [**accettazione**](/windows/desktop/api/Winsock2/nf-winsock2-accept) tramite [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>\_SPXII NSPROTO
</dt> <dd>

SPXII offre una negoziazione di pacchetti Internet di grandi dimensioni per mantenere le dimensioni più adatte per i pacchetti e non richiede l'intervento del programmatore. Tuttavia, se la stazione remota non supporta SPXII e negozia fino a SPX standard, le \_ regole SPX NSPROTO sono attive.



| Protocollo     | File multimediali      | Tipo        | Dimensioni del pacchetto di dati |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | SNAP        |                  |
|              | Token ring | 4 megabit   |                  |
|              |            | 16 megabit  |                  |
| \_SPX NSPROTO | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | SNAP        |                  |
|              | Token ring | 4 megabit   |                  |
|              |            | 16 megabit  |                  |



 

</dd> </dl>

 

 



