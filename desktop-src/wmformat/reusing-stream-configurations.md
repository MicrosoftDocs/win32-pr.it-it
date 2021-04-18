---
title: Riutilizzo delle configurazioni di flusso
description: Riutilizzo delle configurazioni di flusso
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- flussi, riutilizzo delle configurazioni
- profili, riutilizzo delle configurazioni di flusso
- riutilizzo delle configurazioni di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299385"
---
# <a name="reusing-stream-configurations"></a>Riutilizzo delle configurazioni di flusso

Spesso è necessario riutilizzare un oggetto di configurazione del flusso da un profilo esistente. È possibile che siano presenti profili obsoleti che devono essere aggiornati oppure che sia necessario un flusso identico a uno in un profilo di sistema. È più facile riutilizzare le configurazioni di flusso rispetto a crearne di nuove e spesso è possibile modificare alcune impostazioni in una configurazione per soddisfare le proprie esigenze, anziché crearne una completamente nuova.

Tenere presente che esistono alcune limitazioni alla modalità di modifica delle configurazioni di flusso. Se si modificano le impostazioni in modo errato, è possibile che il profilo non accetti l'oggetto di configurazione del flusso. Le configurazioni di flusso non corrette vengono spesso accettate dal profilo, ma fanno in modo che l'oggetto writer rifiuti il profilo. Quando si usano e si modificano le configurazioni di flusso esistenti, tenere presenti le limitazioni e i problemi seguenti.

-   Non modificare mai il contenuto di un file con estensione prx per modificare le impostazioni del flusso. Quando i profili vengono salvati in stringhe XML e scritti in un file con estensione prx, è possibile leggerli con qualsiasi editor di testo. Esaminare un profilo salvato può essere utile per comprendere il funzionamento dei profili. Tuttavia, non è consigliabile modificare mai un file con estensione prx in alcun modo. Anche le modifiche apparentemente banali possono invalidare il profilo.
-   Diverse versioni del codec Windows Media Audio utilizzano le stesse configurazioni di flusso. Se si dispone di un oggetto di configurazione del flusso configurato come sottotipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAUDIOV7 o WMMEDIASUBTYPE \_ WMAudioV8, il flusso risultante verrà compresso con il codec Windows Media audio più recente. Tuttavia, è necessario valutare le proprie esigenze prima di utilizzare un codec audio esistente. Molti tipi di file possono essere migliorati eseguendo l'aggiornamento alla versione più recente del codec Windows Media Audio Professional o il codec Windows Media Audio senza perdita di dati.
-   Non modificare mai il sottotipo di un flusso per eseguire l'aggiornamento a un nuovo codec. Quando si usano i metodi di [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) per ottenere una configurazione del flusso, il codec vi collega alcuni dati che identificano il formato del flusso di bit. Se si modifica il sottotipo di un oggetto di configurazione del flusso esistente, il sottotipo non corrisponderà ai dati del codec. Un profilo con una configurazione di flusso di questo tipo non verrà accettato dall'oggetto writer.
-   Non modificare le impostazioni delle configurazioni del flusso audio compresso. Se le impostazioni di un flusso audio non soddisfano le proprie esigenze, ottenere una nuova configurazione di flusso dal codec usando i metodi di **IWMCodecInfo3**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Recupero delle informazioni di configurazione dei flussi dai codec**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




