---
description: L'oggetto call rappresenta una connessione di indirizzi tra l'indirizzo locale e uno o più indirizzi.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Chiama oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319883"
---
# <a name="call-object"></a>Chiama oggetto

L'oggetto call rappresenta la connessione di un indirizzo tra l'indirizzo locale e uno o più indirizzi. Tutto il controllo delle chiamate viene eseguito tramite l'oggetto call. [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sono le interfacce usate più di frequente nell'oggetto call. Queste interfacce implementano una serie di operazioni e query, ad esempio l'acquisizione di puntatori di interfaccia per flussi multimediali o l'ottenimento dell'ID chiamante. Vedere le sezioni principali della panoramica sulle [operazioni di sessione](session-operations-ovr.md) e informazioni di [sessione](session-information-ovr.md) per le verifiche di quelle supportate da TAPI.

Un provider di servizi multimediali può implementare [interfacce specifiche del provider](provider-specific-interfaces.md), che vengono aggregate in un oggetto chiamata da TAPI. Per informazioni dettagliate sull'implementazione di un provider, vedere la documentazione del provider di servizi.

Gli esempi [effettuare una chiamata](make-a-call.md) e [ricevere un](receive-a-call.md) codice di chiamata mostrano alcune illustrazioni sull'uso di un oggetto call.

Vedere [chiamare le interfacce dell'oggetto](call-object-interfaces.md) per un elenco di tutte le interfacce associate all'oggetto chiamata.

 

 



