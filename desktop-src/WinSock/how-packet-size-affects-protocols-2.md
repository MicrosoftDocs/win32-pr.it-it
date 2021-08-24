---
description: I problemi relativi alle dimensioni dei pacchetti multimediali illustrati nell'argomento Informazioni sulle dimensioni dei pacchetti multimediali influiscono in modo diverso sui vari protocolli \_ IPX PF.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Impatto delle dimensioni dei pacchetti sui protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa654e8884f56ae8079375fa32764ad240f0c870229d07e50623f6e18e42958b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051639"
---
# <a name="how-packet-size-affects-protocols"></a>Impatto delle dimensioni dei pacchetti sui protocolli

I problemi relativi alle dimensioni dei pacchetti multimediali illustrati nell'argomento [Informazioni sulle dimensioni](about-media-packet-size-2.md)dei pacchetti multimediali influiscono in modo diverso sui vari protocolli IPX PF. \_ Una strategia comune per la gestione di vari vincoli di dimensioni del router e dei supporti consiste nell'usare le dimensioni complete dei supporti quando il numero di rete della stazione remota corrisponde alla stazione locale ed eseguire il fall back alla dimensione minima del pacchetto in caso contrario.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

Fornisce un servizio datagrammi; ogni datagramma deve trovarsi entro le dimensioni massime del pacchetto. Winsock imposta le dimensioni massime del pacchetto di datagramma sulla dimensione del pacchetto multimediale locale meno l'intestazione IPX. Tenere presente, tuttavia, che se il pacchetto viene instradato, potrebbe essere raggiunto il router restrizioni durante il routing. Assicurarsi che l'applicazione possa eseguire il fall back a datagrammi a 546 byte.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Fornisce servizi di flusso e di pacchetti sequenziati. Winsock IPX/SPX consente ai flussi di dati e ai messaggi di estendersi su più pacchetti, pertanto le dimensioni dei pacchetti non limitano la quantità di dati gestiti da [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv). Tuttavia, le dimensioni dei supporti sottostanti devono essere impostate correttamente o il primo pacchetto di grandi dimensioni non sarà recapitabile e la connessione verrà reimpostata. Se la stazione di destinazione si trova nella rete locale, Winsock imposta le dimensioni del pacchetto sulle dimensioni del pacchetto multimediale. In caso contrario, il valore predefinito è 512 byte. Queste dimensioni possono essere modificate immediatamente dopo la [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o [**l'accettazione**](/windows/desktop/api/Winsock2/nf-winsock2-accept) tramite [**setockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII offre una negoziazione di pacchetti Internet di grandi dimensioni per mantenere una dimensione ottimale per i pacchetti e non richiede l'intervento del programmatore. Tuttavia, se la stazione remota non supporta SPXII e negozia verso spx standard, le regole SPX NSPROTO \_ sono effettive.



| Protocollo     | File multimediali      | Tipo        | Dimensioni del pacchetto di dati |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | scatto        |                  |
|              | Token ring | 4 megabit   |                  |
|              |            | 16 megabit  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | scatto        |                  |
|              | Token ring | 4 megabit   |                  |
|              |            | 16 megabit  |                  |



 

</dd> </dl>

 

 



