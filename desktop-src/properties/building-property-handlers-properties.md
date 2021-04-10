---
description: Le proprietà sono rappresentate da ID noti come identificatori di proprietà (PID).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Informazioni sui gestori delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564d6f8bd325e649ff1356869932521d8c1cd885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226897"
---
# <a name="understanding-property-handlers"></a>Informazioni sui gestori delle proprietà

Le proprietà sono rappresentate da ID noti come identificatori di proprietà (PID). Ogni proprietà deve avere un identificatore univoco globale (GUID). Questo identificatore è costituito da un GUID, che rappresenta una raccolta di proprietà denominata set di proprietà più una stringa o un Integer a 32 bit per identificare la proprietà all'interno del set. Se viene utilizzato il formato integer dell'ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi. I fornitori possono garantire che le proprie proprietà siano definite in modo univoco inserendole in un set di proprietà definito dai rispettivi GUID.

> [!IMPORTANT]
> È fondamentale definire le proprietà in modo accurato e strategico per il primo rilascio dello schema. Tutte le modifiche apportate alle proprietà personalizzate (ad esempio, la larghezza della colonna o il tipo di proprietà) non verranno riflesse nel database dopo che uno schema è stato registrato. L'unico modo per riconoscere queste modifiche dopo che lo schema è stato registrato una volta in un sistema sarebbe ricompilare l'indice e quindi registrare il nuovo schema oppure per registrare lo schema e quindi creare una nuova proprietà (costituita da un nome canonico e un PKEY) per ogni versione di Subequent; ad esempio `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` e così via). Non è consigliabile creare nuove proprietà in questo modo, perché più colonne estranee potrebbero avere conseguenze sulle prestazioni del sistema.

 

Questo argomento è organizzato nel modo seguente:

-   [Metadata](#metadata)
    -   [Apri metadati](#open-metadata)
-   [Informazioni sui gestori di proprietà](#about-property-handlers)
-   [Tecnologia legacy](#legacy-technology)
-   [Argomenti correlati](#related-topics)

## <a name="metadata"></a>Metadati

In Windows Vista e versioni successive, un nuovo sistema di proprietà basato sui metadati è fondamentale per organizzare elementi quali file, posta elettronica e contatti. In questo nuovo sistema di proprietà è possibile cercare gli elementi in base ai relativi metadati e gli utenti possono leggere o scrivere i metadati. I metadati in questo sistema sono rappresentati da un set estendibile di *Proprietà* implementate come coppie nome/valore.

In Windows Vista e versioni successive, un ampio set di proprietà copre le specifiche di elementi quali foto, musica, documenti, messaggi, contatti e file. I fornitori di software indipendenti (ISV) possono introdurre le proprie proprietà sulla piattaforma se nessuna proprietà esistente soddisfa le proprie esigenze.

### <a name="open-metadata"></a>Apri metadati

Il sistema di proprietà in Windows Vista e versioni successive è un sistema di metadati aperto. Un formato di file archivia qualsiasi proprietà assegnata ed espone tale valore quando viene eseguita una query, indipendentemente dalla pertinenza o dal significato. Ciò consente agli sviluppatori di terze parti di associare proprietà aggiuntive al file senza richiedere una modifica nel gestore proprietà associato. I metadati aperti sono un concetto potente. Per ulteriori informazioni su come supportare i metadati aperti per un formato di file basato su XML, vedere "supporto dei metadati aperti" nell'argomento [inizializzazione dei gestori di proprietà](./building-property-handlers-property-handlers.md).

> [!Note]  
> I gestori di proprietà sono sempre associati a tipi di file specifici; Pertanto, se il formato di file contiene proprietà che richiedono un gestore di proprietà personalizzato, è necessario registrare sempre un'estensione di file univoca per ogni formato di file.

 

## <a name="about-property-handlers"></a>Informazioni sui gestori di proprietà

In Windows Vista e versioni successive, Windows dispone di un sistema di proprietà estendibile per l'archiviazione e il recupero dei metadati nei file e negli elementi di dati a cui si accede. Esplora risorse e il sistema di ricerca di Windows, insieme ad altre applicazioni, utilizzano i gestori delle proprietà per leggere e modificare questi metadati. Se si è uno sviluppatore proprietario di un tipo di file specifico, è necessario registrare un gestore di proprietà per concedere al sistema di proprietà l'accesso ai metadati nei file. In alcuni casi, è possibile utilizzare un gestore di proprietà esistente in grado di leggere e comprendere il formato del file e le relative proprietà. in altri casi, potrebbe essere necessario sviluppare un nuovo gestore di proprietà per il tipo di file.

Il primo passaggio nella scrittura di un gestore proprietà consiste nel considerare le proprietà supportate dal tipo di file. I valori delle proprietà vengono archiviati nel flusso di file, principalmente per consentire la trasportabilità. Quando i valori delle proprietà vengono archiviati nel file stesso, così come sono in questo sistema, un utente può copiare un file in un altro computer, un'unità flash USB o un altro file system o inviare il file come allegato di posta elettronica, le proprietà viaggiano con il file e non vengono mai sincronizzate o perse. Pertanto, se il formato di file supporta l'archiviazione di informazioni aggiuntive, è consigliabile archiviare le proprietà nel file stesso.

Il passaggio successivo consiste nel determinare quali proprietà devono essere fornite dal file. Si potrebbe pensare inizialmente che un set limitato di proprietà sia adeguato. Un file audio potrebbe supportare solo le proprietà relative all'audio e terminarlo. Tuttavia, il file audio potrebbe essere una registrazione di una sessione di un tribunale, archiviata da un legale. In tal caso, l'azienda giuridica avrebbe certamente intenzione di associare altre proprietà non audio a questo file, ad esempio il numero del caso. Il provider del formato di file audio non può probabilmente determinare tutti gli scenari in cui verrà usato il formato. È pertanto consigliabile abilitare l'archiviazione coperta di qualsiasi proprietà arbitraria supportata dal sistema di proprietà.

## <a name="legacy-technology"></a>Tecnologia legacy

La tecnologia Microsoft Windows NT file System (NTFS) del flusso secondario è stata sviluppata per supportare la persistenza di informazioni aggiuntive con il file tramite un flusso alternativo impostato a livello file system. Ci si potrebbe chiedere perché questi flussi secondari non vengono usati come metodo principale per archiviare le proprietà, soprattutto con il supporto dei metadati aperti. Il motivo principale è la trasportabilità di queste informazioni aggiuntive. Sfortunatamente, questi flussi alternativi vengono rimossi in molti scenari, tra cui il supporto per la memorizzazione nella cache lato client (CSC), l'invio di file come allegati e la copia di file in un archivio non NTFS.

I flussi secondari non forniscono una soluzione affidabile in cui si garantisce che le proprietà viaggino con il file e, di conseguenza, il sistema di proprietà di Windows Vista non fornisce un meccanismo incorporato che sfrutta i flussi NTFS secondari per l'archiviazione delle proprietà. Gli ISV sono inoltre altamente sconsigliati dalla creazione di gestori di proprietà che utilizzano flussi secondari per l'archiviazione delle proprietà. Naturalmente, esistono scenari in cui i flussi secondari NTFS sono appropriati, in particolare quando le applicazioni possono garantire che il file che si sta occupando sia sempre archiviato in un volume NTFS e non venga trasmesso in seguito all'interazione con l'utente finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
