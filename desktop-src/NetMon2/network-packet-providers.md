---
description: I provider di pacchetti di rete sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle applicazioni NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Provider di pacchetti di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c580610224a5d6cb3f461b1c039862e49b29358c4952549cefefe3c7434aa084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799537"
---
# <a name="network-packet-providers"></a>Provider di pacchetti di rete

I provider di pacchetti di rete sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle applicazioni [*NPP.*](n.md)

La figura seguente mostra due NPP: il NPP NDIS fornito da Network Monitor e un NPP personalizzato.

![ndis npp fornito da Network Monitor e un npp personalizzato](images/npp.png)

L'NPP NDIS fornito da Network Monitor è Ndisnpp.dll. Questo NPP usa il driver di sistema Network Monitor (Nmnt.sys) per ottenere i frame raccolti dalla rete e diverse interfacce COM (definite interfacce NPP) per passare i frame all'interfaccia utente di Network Monitor e alle applicazioni NPP, in cui possono essere visualizzati e analizzati.

Ndisnpp.dll si connette al livello [*NDIS*](n.md) per ottenere il traffico di rete. I provider di servizi di rete personalizzati possono ignorare il livello NDIS e comunicare direttamente con l'hardware di rete. Tenere presente che, indipendentemente dal fatto che un NPP usi NDIS, i provider di servizi di rete possono connettersi a un numero qualsiasi di schede di rete e che tutti i server dei criteri di rete devono supportare le stesse interfacce NPP.

Prima che un'applicazione possa iniziare ad acquisire dati, deve:

-   Selezionare la scheda di interfaccia di rete (NIC) che connetterà NPP alla rete.
-   Selezionare l'interfaccia NPP che verrà usata per acquisire i frame di rete.
-   Usare l'interfaccia selezionata per connettersi alla scheda di interfaccia di rete.

Per altre informazioni su come enumerare e selezionare una scheda di interfaccia di rete, vedere [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md).

Per altre informazioni sulle interfacce COM esposte dai provider di servizi di rete, vedere [Selezione di un'interfaccia NPP.](selecting-an-npp-interface.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStat**](istats.md)
</dt> </dl>

 

 



