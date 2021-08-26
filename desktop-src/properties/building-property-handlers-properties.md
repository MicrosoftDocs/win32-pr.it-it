---
description: Le proprietà sono rappresentate da ID noti come identificatori di proprietà (PID).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Informazioni sui gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42139a869551f0f4dc786f02c66c673a49495ba01f5258aeeff12051bd3f60b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946971"
---
# <a name="understanding-property-handlers"></a>Informazioni sui gestori di proprietà

Le proprietà sono rappresentate da ID noti come identificatori di proprietà (PID). Ogni proprietà DEVE avere un identificatore univoco globale (GUID). Questo identificatore è costituito da un GUID, che rappresenta una raccolta di proprietà denominata set di proprietà più una stringa o un intero a 32 bit per identificare la proprietà all'interno del set. Se viene usato il formato intero di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi. I fornitori possono garantire che le relative proprietà siano definite in modo univoco inserendole in un set di proprietà definito dai propri GUID.

> [!IMPORTANT]
> È fondamentale definire le proprietà con attenzione e in modo strategico per la prima versione dello schema. Eventuali modifiche alle proprietà personalizzate, ad esempio la larghezza della colonna o il tipo di proprietà, non verranno riflesse nel database dopo la registrazione di uno schema. L'unico modo per fare in modo che queste modifiche riconosca dopo che lo schema è stato registrato una volta in un sistema consiste nel ricompilare l'indice e quindi registrare il nuovo schema oppure registrare lo schema e quindi creare una nuova proprietà (costituita da un nome canonico e da una chiave PKEY) per ogni versione secondaria; ad esempio `PKEY_GroupName_PropertyNameV2` `PKEY_GroupName_PropertyNameV3` , e così via). Non è consigliabile creare nuove proprietà in questo modo, perché più colonne estranee possono influire sulle prestazioni del sistema.

 

Questo argomento è organizzato come segue:

-   [Metadata](#metadata)
    -   [Aprire i metadati](#open-metadata)
-   [Informazioni sui gestori di proprietà](#about-property-handlers)
-   [Tecnologia legacy](#legacy-technology)
-   [Argomenti correlati](#related-topics)

## <a name="metadata"></a>Metadati

In Windows Vista e versioni successive, un nuovo sistema di proprietà basato sui metadati è fondamentale per organizzare elementi quali file, messaggi di posta elettronica e contatti. In questo nuovo sistema di proprietà è possibile cercare gli elementi in base ai relativi metadati e gli utenti possono leggere o scrivere tali metadati. I metadati in questo sistema sono rappresentati da un set estendibile di *proprietà* implementate come coppie nome/valore.

In Windows Vista e versioni successive, un set completo di proprietà include le specifiche di elementi come foto, musica, documenti, messaggi, contatti e file. I fornitori di software indipendenti (ISV) possono introdurre le proprie proprietà nella piattaforma se nessuna proprietà esistente soddisfa le proprie esigenze.

### <a name="open-metadata"></a>Aprire i metadati

Il sistema di proprietà in Windows Vista e versioni successive è un sistema di metadati aperto. Un formato di file archivia qualsiasi proprietà assegnata ed espone tale valore quando viene eseguita una query, indipendentemente dalla pertinenza o dal significato. In questo modo gli sviluppatori di terze parti possono allegare proprietà aggiuntive al file senza richiedere una modifica nel gestore delle proprietà associato. I metadati aperti sono un concetto potente. Per altre informazioni su come supportare i metadati aperti per un formato di file basato su XML, vedere "Supporto dei metadati aperti" in Inizializzazione di [gestori di proprietà.](./building-property-handlers-property-handlers.md)

> [!Note]  
> I gestori di proprietà sono sempre associati a tipi di file specifici. Pertanto, se il formato di file contiene proprietà che richiedono un gestore delle proprietà personalizzate, è sempre necessario registrare un'estensione di file univoca per ogni formato di file.

 

## <a name="about-property-handlers"></a>Informazioni sui gestori di proprietà

In Windows Vista e versioni successive, Windows dispone di un sistema di proprietà estendibile per l'archiviazione e il recupero di metadati nei file e negli elementi di dati a cui si accede. Windows Explorer e il Windows di ricerca, insieme ad altre applicazioni, usano gestori di proprietà per leggere e modificare questi metadati. Gli sviluppatori proprietari di un tipo di file specifico devono registrare un gestore delle proprietà per concedere al sistema di proprietà l'accesso ai metadati nei file. In alcuni casi, potrebbe essere possibile usare un gestore delle proprietà esistente in grado di leggere e comprendere il formato di file e le relative proprietà. In altri casi, potrebbe essere necessario sviluppare un nuovo gestore delle proprietà per il tipo di file.

Il primo passaggio per scrivere un gestore delle proprietà consiste nel considerare le proprietà supportate dal tipo di file. I valori delle proprietà vengono archiviati nel flusso di file, principalmente per abilitare il trasporto. Quando i valori delle proprietà vengono archiviati nel file stesso, così come sono in questo sistema, un utente può copiare un file in un altro computer, in un'unità flash USB o in un altro file system oppure invia il file come allegato di posta elettronica, le proprietà si spostano con il file e non vengono mai sincronizzate o perse. Pertanto, se il formato di file supporta l'archiviazione di informazioni aggiuntive, è meglio archiviare le proprietà nel file stesso.

Il passaggio successivo consiste nel determinare le proprietà che il file deve fornire. Inizialmente si potrebbe pensare che un set limitato di proprietà sia adeguato. Un file audio può supportare solo le proprietà relative all'audio e termina qui. Tuttavia, tale file audio potrebbe essere una registrazione di una sessione di un processo legale, archiviata da uno studio legale. In tal caso, lo studio legale vuole sicuramente associare altre proprietà non audio a questo file, ad esempio il numero del caso. Il provider del formato di file audio non può determinare tutti gli scenari in cui il formato verrà usato. È quindi consigliabile abilitare l'archiviazione di qualsiasi proprietà arbitraria supportata dal sistema di proprietà.

## <a name="legacy-technology"></a>Tecnologia legacy

È stata sviluppata la tecnologia di flusso secondario Microsoft Windows NT File System (NTFS) per supportare la persistenza di informazioni aggiuntive con il file tramite un flusso alternativo impostato a file system livello. Ci si potrebbe chiedere perché questi flussi secondari non vengono usati come metodo principale per archiviare le proprietà, in particolare con il supporto dei metadati aperti. Il motivo principale è la trasportabilità di queste informazioni aggiuntive. Sfortunatamente, questi flussi alternativi vengono rimossi in molti scenari, tra cui il supporto della memorizzazione nella cache sul lato client (CSC), l'invio di file come allegati e la copia di file in un archivio non NTFS.

I flussi secondari non offrono una soluzione affidabile in cui le proprietà possono essere trasmesse con il file e, di conseguenza, il sistema di proprietà di Windows Vista non fornisce un meccanismo predefinito che sfrutta i flussi NTFS secondari per l'archiviazione delle proprietà. È anche sconsigliato creare gestori di proprietà che usano flussi secondari per l'archiviazione delle proprietà. Esistono naturalmente scenari in cui i flussi secondari NTFS sono appropriati, in particolare quando le applicazioni possono garantire che il file che gestiscono sia sempre archiviato in un volume NTFS e non si spostano in seguito all'interazione dell'utente finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di nomi di tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
