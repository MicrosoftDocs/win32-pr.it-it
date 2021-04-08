---
description: Questo argomento contiene informazioni sulla programmazione. Nell'elenco seguente sono indicati alcuni suggerimenti per la programmazione che consentono di scrivere un parser.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Considerazioni sulla programmazione (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213104060f7dd3c6b6dbe56d22044508e0878c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756215"
---
# <a name="programming-considerations-network-monitor"></a>Considerazioni sulla programmazione (Network Monitor)

Questo argomento contiene informazioni sulla programmazione. Nell'elenco seguente sono indicati alcuni suggerimenti per la programmazione che consentono di scrivere un parser.



|                                                 |                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Installazione automatica del parser                     | Implementare la funzione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) per installare automaticamente il parser e aggiornare i file ini associati. Se si installa il parser manualmente, è necessario aggiornare manualmente tutti i file INI associati.                                                                                                                                                          |
| Analisi delle proprietà del protocollo                     | Implementare la funzione [**AttachProperties**](attachproperties.md) per analizzare le proprietà del protocollo. Evitare di usare la funzione [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando si collega un'istanza di proprietà e usarla solo per i dati non allineati ai byte o per i dati che devono essere decodificati. Per la connessione di proprietà si intende il mapping di un'istanza di proprietà a una posizione specifica in un'acquisizione. |
| Analisi dei protocolli suddivisi tra frame | Si supponga che ogni parte del protocollo sia completa all'interno di un frame e si presupponga che l'utente chiami lo strumento COALESCE protocollo per combinare le parti in un unico protocollo. Non esaminare un frame precedente durante l'analisi di un protocollo ed evitare di provare a ricostruire un protocollo diviso tra frame.                                                                                              |
| Formattazione dei dati visualizzati                       | Chiamare la funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per utilizzare il formattatore generico per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. Evitare di scrivere un formattatore personalizzato per i dati di visualizzazione dell'interfaccia utente. Tuttavia, è possibile chiamare un formattatore personalizzato per creare una riga di [*proprietà di riepilogo*](s.md) per il protocollo che si sta analizzando.            |
| Uso di CCAlloc                                   | Utilizzare CCAlloc quando si desidera che Network Monitor allocare i dati in base all'acquisizione. Network Monitor non specifica l'ordine in base al quale i frame chiamano il parser.                                                                                                                                                                                                                                                |
| Mantenimento senza stato del parser                      | Mantieni l'operazione del parser senza stato, perché quando Network Monitor analizza un'acquisizione, i frame non vengono passati al parser in un ordine specifico. Per questo motivo, è consigliabile non mantenere i dati globali.                                                                                                                                                                                      |



 

 

 



