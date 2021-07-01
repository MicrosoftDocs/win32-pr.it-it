---
description: Questo argomento contiene informazioni sulla programmazione. L'elenco seguente identifica alcuni suggerimenti per la programmazione che consentono di scrivere un parser.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Considerazioni sulla programmazione (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2deb53a27d8abda4f45663b65fb922600a5b5386
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120226"
---
# <a name="programming-considerations-network-monitor"></a>Considerazioni sulla programmazione (Network Monitor)

Questo argomento contiene informazioni sulla programmazione. L'elenco seguente identifica alcuni suggerimenti per la programmazione che consentono di scrivere un parser.



| Suggerimento                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Installazione automatica del parser                     | Implementare [**la funzione ParserAutoInstallInfo**](parserautoinstallinfo.md) per installare automaticamente il parser e aggiornare i file INI associati. Se si installa manualmente il parser, è necessario aggiornare manualmente tutti i file INI associati.                                                                                                                                                          |
| Analisi delle proprietà del protocollo                     | Implementare [**la funzione AttachProperties**](attachproperties.md) per analizzare le proprietà del protocollo. Evitare di usare [**la funzione AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando si collega un'istanza di proprietà e usarla solo per dati non allineati a byte o dati che devono essere decodificati. Per associazione di proprietà si intende il mapping di un'istanza di proprietà a una posizione specifica in un'acquisizione. |
| Protocolli di analisi suddivisi tra frame | Si supponga che ogni parte del protocollo sia completa all'interno di un frame e presupponga che l'utente chiami lo strumento Protocol Coalesce per combinare le parti in un unico protocollo. Non esaminare un frame precedente durante l'analisi di un protocollo ed evitare di tentare di ricostruire un protocollo suddiviso tra frame.                                                                                              |
| Formattazione dei dati visualizzati                       | Chiamare la [**funzione FormatPropertyInstance**](formatpropertyinstance.md) per usare il formattatore generico per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente. Evitare di scrivere un formattatore personalizzato per i dati di visualizzazione dell'interfaccia utente. Tuttavia, è possibile chiamare un formattatore personalizzato per creare una riga di [*proprietà*](s.md) di riepilogo per il protocollo che si sta analizzando.            |
| Uso di CCAlloc                                   | Usare CCAlloc quando si Network Monitor allocare i dati in base all'acquisizione. Network Monitor non specifica l'ordine in cui i frame chiamano il parser.                                                                                                                                                                                                                                                |
| Mantenimento di un parser senza stato                      | Mantenere l'operazione del parser senza stato perché quando Network Monitor analizza un'acquisizione, non passa i frame al parser in un ordine specifico. Per questo motivo, è consigliabile non conservare i dati globali.                                                                                                                                                                                      |



 

 

 



