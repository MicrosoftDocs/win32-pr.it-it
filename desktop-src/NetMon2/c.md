---
description: Glossario dei termini Network Monitor che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311639"
---
# <a name="c-network-monitor"></a>C (Network Monitor)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**catturare**
</dt> <dd>

Dati relativi al traffico di rete raccolti in frame. Un provider di pacchetti di rete (NPP) esegue un'acquisizione. Vedere anche [*acquisizione ritardata*](d.md)e *acquisizione in tempo reale*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**Acquisisci file**
</dt> <dd>

File creato da Network Monitor per archiviare i dati acquisiti. L'estensione del nome file. Cap identifica un file di acquisizione. Network Monitor genera in modo casuale un nome file di acquisizione, ma è possibile modificare il nome del file quando si salva il file di acquisizione.

Network Monitor crea un file di acquisizione ogni volta che il processo di acquisizione viene avviato e quindi mantiene aperto il file durante il processo di acquisizione. Non è possibile accedere al contenuto di un file di acquisizione finché il processo di acquisizione non viene arrestato e il file di acquisizione viene chiuso.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro di acquisizione**
</dt> <dd>

Set di funzioni Network Monitor utilizzate per limitare i frame in ingresso utilizzati da un'applicazione di provider di pacchetti di rete (NPP).

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**trigger di acquisizione**
</dt> <dd>

Evento trigger impostato per arrestare il processo di acquisizione. L'evento di acquisizione del trigger può essere un file di acquisizione temporaneo indirizzato a un livello specifico o a un modello di dati che si verifica in un frame acquisito.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**dati acquisiti**
</dt> <dd>

Frame che dispongono di un set definito di criteri. I frame di dati sono contenuti in un file di acquisizione temporaneo.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Statistiche sulle conversazioni**
</dt> <dd>

Statistiche del traffico di rete salvato durante un'acquisizione. Queste statistiche includono le informazioni sulle stazioni e sulle sessioni che iniziano quando il processo di acquisizione viene avviato e terminano quando l'acquisizione viene arrestata. Se si sospende il processo di acquisizione, Network Monitor continua ad aggiungere statistiche quando si riprende il processo. Per recuperare le statistiche di conversazione, chiamare il metodo **GetConversationStatistics** per l'interfaccia in uso.

</dd> </dl>

 

 



