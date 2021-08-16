---
description: Glossario dei Network Monitor termini che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31993c18307ab1beaa1b6cff379626b9398987d6ad9475947c4aeb4d09dd32e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367437"
---
# <a name="c-network-monitor"></a>C (Network Monitor)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**Catturare**
</dt> <dd>

Dati sul traffico di rete raccolti in frame. Un provider di pacchetti di rete (NPP) esegue un'acquisizione. Vedere anche [*l'acquisizione ritardata*](d.md)e *l'acquisizione in tempo reale*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**file di acquisizione**
</dt> <dd>

File creato Network Monitor per archiviare i dati acquisiti. L'estensione cap identifica un file di acquisizione. Network Monitor genera in modo casuale un nome file di acquisizione, ma è possibile modificare il nome del file quando si salva il file di acquisizione.

Network Monitor crea un file di acquisizione a ogni avvio del processo di acquisizione e quindi lo mantiene aperto durante il processo di acquisizione. Non è possibile accedere al contenuto di un file di acquisizione finché il processo di acquisizione non viene arrestato e il file di acquisizione non viene chiuso.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro di acquisizione**
</dt> <dd>

Set di funzioni Network Monitor per limitare i frame in ingresso usati da un'applicazione NPP (Network Packet Provider).

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**trigger di acquisizione**
</dt> <dd>

Evento trigger impostato per arrestare il processo di acquisizione. L'evento trigger di acquisizione può essere un file di acquisizione temporaneo che viene indirizzato a un livello specifico o a un modello di dati che si verifica in un frame acquisito.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**dati acquisiti**
</dt> <dd>

Frame con un set definito di criteri. I frame di dati sono contenuti in un file di acquisizione temporaneo.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**statistiche di conversazione**
</dt> <dd>

Statistiche del traffico di rete salvato durante un'acquisizione. Queste statistiche includono informazioni sulla stazione e sulla sessione che iniziano all'avvio del processo di acquisizione e terminano quando l'acquisizione viene arrestata. Se si sospende il processo di acquisizione, Network Monitor continua ad aggiungere statistiche quando si riprende il processo. Per recuperare le statistiche della conversazione, **chiamare il metodo GetConversationStatistics** per l'interfaccia in uso.

</dd> </dl>

 

 



