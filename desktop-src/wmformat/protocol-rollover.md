---
title: Rollover del protocollo
description: Rollover del protocollo
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows Media Format SDK, rollover del protocollo
- ASF (Advanced Systems Format), rollover del protocollo
- ASF (formato avanzato dei sistemi), rollover del protocollo
- rollover del protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046312"
---
# <a name="protocol-rollover"></a>Rollover del protocollo

Il rollover del protocollo è un processo in cui l'oggetto Reader individua il protocollo di streaming migliore disponibile da un server. Il lettore usa il rollover del protocollo ogni volta che viene aperto un URL che contiene uno schema "MMS".

Il lettore supporta diversi protocolli:

-   Protocollo RTSP (Real Time Streaming Protocol)
-   Hypertext Transfer Protocol (HTTP)
-   Microsoft Media Server (MMS)

I protocolli RTSP e MMS sono entrambi disponibili in due versioni, una con [*UDP*](wmformat-glossary.md) come protocollo di recapito sottostante e l'altra con TCP.

L'oggetto Reader usa sempre TCP per i comandi di controllo della riproduzione, ma può usare TCP o UDP per il recapito del contenuto trasmesso. Per la distribuzione del contenuto è preferibile il protocollo UDP, perché impone un sovraccarico della larghezza di banda inferiore rispetto a TCP. Il protocollo TCP garantisce un trasporto affidabile attraverso l'uso di "circuiti virtuali", ma il costo di questa operazione significa che TCP non è altrettanto adatto per i flussi multimediali digitali, in cui l'uso efficiente della larghezza di banda è più importante per i pacchetti persi occasionali.

Quando un URL specifica "mms://", il lettore tenta di usare i protocolli seguenti per il recapito dei dati, nell'ordine seguente:

1.  RTSPt (RTSP con UDP)
2.  RTSPt (RTSP con TCP)
3.  MMSU (MMS con UDP)
4.  MMST (MMS con TCP)
5.  HTTP

HTTP è un protocollo unidirezionale basato su TCP ed è il protocollo utilizzato dai server Web. Lo streaming con HTTP è meno efficiente rispetto all'uso di RTSP. Tuttavia, la maggior parte dei firewall è configurata per accettare richieste HTTP, mentre in genere rifiutano altri protocolli di streaming.

Windows Media Services 9 Series in Microsoft Windows Server 2003 rifiuterà tutte le richieste MMSU o MMST da un lettore di Windows Media Format SDK, perché RTSP è il protocollo di streaming preferito. I servizi Windows Media versione 4,1 e versioni precedenti non supportano RTSP. In questo caso l'oggetto Reader esegue il fallback a MMSU o HTTP.

Il rollover del protocollo non si applica se lo schema URL fornisce un protocollo specifico, ad esempio "rtspu://" per RTSPr o "https://" per HTTP. Se lo schema dell'URL è "rtsp://", il lettore cerca RTSPt e RTSPt, ma non altri.

Quando il lettore apre un file, è possibile eseguire una query sul protocollo usato chiamando il metodo [**IWMReaderAdvanced2:: Getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) sul Reader. Durante lo streaming o il download del contenuto, questo metodo restituisce il nome non appena il contenuto viene memorizzato nella cache completamente, il metodo **Getprotocolname** restituisce la stringa "cache".

Per ottenere i nomi di tutti i protocolli di Windows Media Server supportati dal lettore, chiamare il metodo [**IWMReaderNetworkConfig:: GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) sul Reader. È possibile disabilitare uno o più protocolli nell'elenco di rollover del protocollo del lettore usando l'interfaccia **IWMReaderNetworkConfig** . Ad esempio, il metodo [**IWMReaderNetworkConfig:: SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) Abilita o Disabilita i protocolli basati su TCP e [**IWMReaderNetworkConfig:: SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) Abilita o Disabilita i protocolli basati su UDP. Questi metodi si applicano solo al rollover del protocollo. i protocolli sono ancora disponibili se lo schema URL contiene un protocollo specifico. In genere non esiste alcun motivo per disabilitare i protocolli utilizzati nel rollover del protocollo. Questa operazione può comportare un peggioramento delle prestazioni. Tuttavia, potrebbe essere utile per i test.

 

 




