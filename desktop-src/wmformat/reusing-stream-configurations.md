---
title: Riutilizzo delle configurazioni dei flussi
description: Riutilizzo delle configurazioni dei flussi
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- flussi, riutilizzo di configurazioni
- profili, riutilizzo delle configurazioni dei flussi
- riutilizzo delle configurazioni dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ee1a2b51d5a2a659cb24955ab74a5fb285308125b21781c9d42a709d7e4b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110191"
---
# <a name="reusing-stream-configurations"></a>Riutilizzo delle configurazioni dei flussi

Spesso si vuole riutilizzare un oggetto di configurazione del flusso da un profilo esistente. È possibile che siano presenti profili vecchi che necessitano di aggiornamento o che sia necessario un flusso identico a uno in un profilo di sistema. È più semplice riutilizzare le configurazioni di flusso che crearne di nuove ed è spesso possibile modificare alcune impostazioni in una configurazione per soddisfare le proprie esigenze anziché crearne una completamente nuova.

Tenere presente che esistono limitazioni per la modifica delle configurazioni del flusso. Se si modificano le impostazioni in modo errato, il profilo potrebbe non accettare l'oggetto di configurazione del flusso. Le configurazioni di flusso errate vengono spesso accettate dal profilo, ma causano il rifiuto del profilo da parte dell'oggetto writer. Tenere presenti le limitazioni e i problemi seguenti quando si usano e si modificano le configurazioni di flusso esistenti.

-   Non modificare mai il contenuto di un file prx per modificare le impostazioni del flusso. Quando i profili vengono salvati in stringhe XML e scritti in un file prx, possono essere letti con qualsiasi editor di testo. La visualizzazione di un profilo salvato consente di comprendere il funzionamento dei profili. Tuttavia, non è mai necessario modificare un file con estensione prx in alcun modo. Anche modifiche apparentemente semplici possono invalidare il profilo.
-   Diverse versioni del codec Windows Media Audio usano le stesse configurazioni del flusso. Se si dispone di un oggetto di configurazione del flusso configurato come sottotipo WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAudioV7 o WMMEDIASUBTYPE WMAudioV8, il flusso risultante verrà compresso con il codec audio multimediale \_ Windows più recente. È tuttavia consigliabile valutare le proprie esigenze prima di usare un codec audio esistente. Molti tipi di file possono essere migliorati eseguendo l'aggiornamento alla versione più recente del codec Professional audio multimediale Windows o al codec Windows Media Audio Lossless.
-   Non modificare mai il sottotipo di un flusso per eseguire l'aggiornamento a un nuovo codec. Quando si usano i metodi di [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) per ottenere una configurazione del flusso, il codec allega alcuni dati che identificano il formato del flusso di bit. Se si modifica il sottotipo di un oggetto di configurazione del flusso esistente, il sottotipo non corrisponderà ai dati del codec. Un profilo con tale configurazione del flusso non verrà accettato dall'oggetto writer.
-   Non modificare le impostazioni delle configurazioni del flusso audio compresso. Se le impostazioni di un flusso audio non soddisfano le proprie esigenze, ottenere una nuova configurazione del flusso dal codec usando i metodi **di IWMCodecInfo3.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Recupero delle informazioni di configurazione del flusso dai codec**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




