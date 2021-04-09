---
description: I provider di pacchetti di rete (centrali) sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle applicazioni NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Provider di pacchetti di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885469"
---
# <a name="network-packet-providers"></a>Provider di pacchetti di rete

I provider di pacchetti di rete (centrali) sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle [*applicazioni NPP*](n.md).

Nella figura seguente vengono illustrati due centrali: la NPP di NDIS fornita da Network Monitor e un NPP personalizzato.

![NPP di NDIS fornito da Network Monitor e da un NPP personalizzato](images/npp.png)

Viene Ndisnpp.dll la NPP di NDIS fornita da Network Monitor. Questo NPP usa il driver di sistema Network Monitor (Nmnt.sys) per ottenere i frame raccolti dalla rete e diverse interfacce COM (definite interfacce NPP) per passare i frame all'interfaccia utente Network Monitor e le applicazioni NPP, dove possono essere visualizzate e analizzate.

Ndisnpp.dll si connette al livello [*NDIS*](n.md) per ottenere il traffico di rete. (Centrali personalizzato può ignorare il livello NDIS e comunicare direttamente con l'hardware di rete). Tenere presente che, indipendentemente dal fatto che un NPP usi NDIS, centrali può connettersi a un numero qualsiasi di schede di rete e tutti i centrali devono supportare le stesse interfacce NPP.

Prima che un'applicazione possa iniziare a acquisire i dati, è necessario:

-   Selezionare la scheda di interfaccia di rete (NIC) che collegherà l'NPP alla rete.
-   Selezionare l'interfaccia NPP che verrà usata per acquisire i frame di rete.
-   Usare l'interfaccia selezionata per connettersi alla scheda di interfaccia di rete.

Per ulteriori informazioni su come enumerare e selezionare una scheda di interfaccia di rete, vedere [selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md).

Per ulteriori informazioni sulle interfacce COM esposte da centrali, vedere [selezione di un'interfaccia NPP](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



