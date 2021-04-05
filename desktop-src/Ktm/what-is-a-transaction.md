---
description: 'Una transazione è un gruppo di operazioni che hanno le proprietà seguenti: Atomic, consistent, isolated e Durable (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: Che cos'è una transazione?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881209"
---
# <a name="what-is-a-transaction"></a>Che cos'è una transazione?

Una transazione è un gruppo di operazioni che hanno le proprietà seguenti: Atomic, consistent, isolated e Durable (ACID). Il supporto delle transazioni consente di sviluppare nuovi tipi di applicazioni, semplificando il processo di sviluppo e rendendo l'applicazione più affidabile. Nella parte restante di questo argomento sono disponibili scenari in cui viene illustrata la necessità di queste proprietà, quindi una tabella che definisce ciascuna proprietà.

In un gruppo *atomico* di operazioni, ogni operazione del gruppo deve avere esito positivo oppure gli effetti di tutti questi elementi devono essere annullati (noto anche come *rollback).* Un trasferimento bancario, ad esempio, deve essere un set atomico di due operazioni: un addebito da un account e un credito a un altro account. Il debito e il credito devono essere implementati come gruppi atomici. Se queste due operazioni non hanno entrambe esito positivo, il trasferimento non è corretto a favore della banca o del titolare dell'account.

Il requisito di *coerenza* significa che i dati sono coerenti dopo la transazione (presupponendo che sia stato avviato un sistema coerente prima della transazione). Per l'esempio Bank Transfer, la coerenza può essere definita in modo che il saldo del conto combinato dei due account sia una costante. Per implementare la coerenza nell'esempio Bank Transfer, le operazioni di addebito e di credito devono essere semplicemente per la stessa quantità di denaro.

Un altro esempio di transazione è un aggiornamento a un sito Web. Un sito di commercio elettronico richiede che una nuova pagina di navigazione della categoria di prodotto appaia esattamente allo stesso tempo delle pagine dei dettagli del prodotto che descrivono i nuovi prodotti. In questo caso, è necessario aggiornare e aggiungere più voci di directory sotto il controllo di una transazione. Non solo è necessario che gli aggiornamenti siano atomici, ma è anche necessario che un cliente che attualmente acquisti non debba visualizzare gli aggiornamenti in corso. Questo è un esempio della proprietà di *isolamento* delle transazioni.

Per la proprietà della *durabilità* è necessario che, al termine di un aggiornamento, i relativi effetti vengano mantenuti anche se il sistema smette di rispondere. Nell'esempio precedente, la durabilità può essere garantita semplicemente garantendo un ripristino dei dati adeguato, in modo che tutte le nuove file system voci che rappresentano l'aggiunta di un nuovo prodotto al sito vengano visualizzate dopo che un sistema smette di rispondere. Questa operazione richiede un sistema con meccanismi di backup, ripristino e disponibilità elevata dei dati.

La garanzia dell'atomicità di una transazione, nonché delle altre proprietà, è presente in un numero qualsiasi di errori, inclusi gli errori che si verificano durante la fase di recupero di un errore precedente. Infine, il sistema raggiungerà uno dei due stati seguenti: tutte le operazioni sono state applicate o nessuna delle operazioni è stata applicata.

Nella tabella seguente sono riepilogate le proprietà di una transazione.



| Termine                                                                                                         | Descrizione                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomica<br/>                 | Tutte le operazioni nella transazione hanno esito positivo o nessuna delle operazioni viene mantenute.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente<br/> | Se i dati sono coerenti prima che inizi la transazione, saranno coerenti al termine della transazione.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isolato <br/>     | Gli effetti di una transazione in corso sono nascosti da tutte le altre transazioni.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durevole<br/>             | Quando una transazione viene completata, i risultati sono persistenti e sopravvivono a un arresto anomalo del sistema.<br/>                               |



 

Queste proprietà assicurano che il software sia in grado di gestire gli errori imprevisti, poiché può semplicemente interrompere una transazione quando una situazione imprevista impedisce il corretto completamento. L'infrastruttura di transazione garantisce che venga eseguito il rollback di tutti gli effetti della transazione interrotta, restituendo i dati a uno stato coerente. Pertanto, un sistema transazionale consente un ripristino normale dagli errori di sistema.

Per garantire le proprietà ACID, un sistema che supporta le transazioni deve disporre di una funzionalità di registrazione affidabile che può essere utilizzata per eseguire il commit o il rollback delle transazioni in caso di necessità. Per ulteriori informazioni, vedere [Common Log file System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

