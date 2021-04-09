---
description: PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e in caso contrario implementarne le funzionalità multicast.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opzioni socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879189"
---
# <a name="pgm-socket-options"></a>Opzioni socket PGM

PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e in caso contrario implementarne le funzionalità multicast. Questa pagina specifica come impostare le opzioni del socket PGM, enumera le opzioni del socket disponibili per PGM e, laddove appropriato, fornisce esempi di utilizzo e informazioni aggiuntive per le varie opzioni. Per le definizioni di base di ogni opzione del socket PCM, vedere [Opzioni di socket](socket-options.md).

**Windows XP:** La programmazione del multicast affidabile (PGM) non è supportata.

Per i mittenti PGM sono disponibili le seguenti opzioni di socket:

<dl> \_LATEJOIN RM  
\_dimensioni della \_ finestra \_ velocità RM  
\_ \_ frequenza ADV della finestra di trasmissione RM \_ \_  
\_statistiche mittente \_ RM  
\_ \_ \_ Metodo Advance della finestra mittente RM \_  
RM \_ impostare \_ mcast \_ TTL  
\_ \_ limite messaggi set \_ RM  
RM \_ impostare \_ Invia \_ se  
\_usare \_ FEC per RM  
</dl>

L' \_ opzione del \_ Metodo Advance della finestra mittente RM \_ \_ specifica il metodo utilizzato per l'avanzamento della finestra di invio del bordo finale. Il parametro optVal può essere impostato solo \_ \_ su E la finestra avanza \_ per \_ ora (impostazione predefinita). Si noti che \_ l' \_ uso \_ della finestra E come \_ cache dei dati \_ non è supportato.

Per i ricevitori PGM sono disponibili le seguenti opzioni di socket:

<dl> RM \_ Aggiungi \_ ricezione \_ se  
RM \_ del \_ Receive \_ se  
\_opt per Intranet ad alta \_ velocità \_ \_  
\_statistiche ricevitore \_ RM  
</dl>

## <a name="setting-pgm-socket-options"></a>Impostazione delle opzioni del socket PGM

Il frammento di codice seguente illustra una guida di programmazione per l'impostazione delle opzioni del socket PGM:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



Nel frammento di codice precedente, il tipo e il contenuto di *OptionData* dipendono dall'opzione socket da impostare. Per tutte le opzioni del socket PGM, il livello di socket è IPPROTO \_ RM. È necessario impostare le opzioni del socket PGM immediatamente dopo la chiamata alla funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , con le eccezioni seguenti:

<dl> \_ \_ limite messaggi set \_ RM  
\_statistiche mittente \_ RM  
\_statistiche ricevitore \_ RM  
</dl>

 

 



