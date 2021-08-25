---
description: PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e implementare in altro modo le funzionalità multicast.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opzioni socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e8df8050146774ac79d45594adcccf53a93d295ce42b9f00834aa0d699e83a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860821"
---
# <a name="pgm-socket-options"></a>Opzioni socket PGM

PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e implementare in altro modo le funzionalità multicast. Questa pagina specifica come impostare le opzioni del socket PGM, enumera le opzioni socket disponibili per PGM e, dove appropriato, fornisce esempi di utilizzo e informazioni aggiuntive per le varie opzioni. Per le definizioni di base di ogni opzione del socket PCM, vedere [Opzioni socket.](socket-options.md)

**Windows XP:** Reliable Multicast Programming (PGM) non è supportato.

Per i mittenti PGM sono disponibili le opzioni socket seguenti:

<dl> RM \_ LATEJOIN  
DIMENSIONI DELLA \_ FINESTRA \_ FREQUENZA \_ RM  
FREQUENZA \_ \_ ADV DELLA \_ FINESTRA DI INVIO \_ RM  
STATISTICHE RM \_ MITTENTE \_  
METODO ADVANCE \_ DELLA \_ FINESTRA MITTENTE \_ \_ RM  
RM \_ SET \_ MCAST \_ TTL  
LIMITE DEL \_ MESSAGGIO RM SET \_ \_  
RM \_ SET \_ SEND \_ IF  
RM \_ USE \_ FEC  
</dl>

L'opzione RM SENDER WINDOW ADVANCE METHOD specifica il metodo usato per far avanzare la \_ finestra di invio edge \_ \_ \_ finale. Il parametro optval può essere solo E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (impostazione predefinita). Si noti che E \_ WINDOW USE AS DATA CACHE non è \_ \_ \_ \_ supportato.

Per i ricevitori PGM sono disponibili le opzioni socket seguenti:

<dl> RM \_ ADD \_ RECEIVE \_ IF  
RM \_ DEL \_ RECEIVE \_ IF  
RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT  
STATISTICHE \_ RICEVITORE \_ RM  
</dl>

## <a name="setting-pgm-socket-options"></a>Impostazione delle opzioni del socket PGM

Il frammento di codice seguente illustra una linea guida per la programmazione per l'impostazione delle opzioni socket PGM:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



Nel frammento di codice precedente il tipo e il contenuto di *OptionData* dipendono dall'opzione socket impostata. Per tutte le opzioni socket PGM, il livello del socket è IPPROTO \_ RM. Le opzioni del socket PGM devono essere impostate immediatamente dopo la chiamata alla funzione [**di**](/windows/desktop/api/winsock/nf-winsock-bind) associazione, con le eccezioni seguenti:

<dl> LIMITE DEL \_ MESSAGGIO RM SET \_ \_  
STATISTICHE RM \_ MITTENTE \_  
STATISTICHE \_ RICEVITORE \_ RM  
</dl>

 

 



