---
description: 'Una transazione è un gruppo di operazioni con le proprietà seguenti: atomica, coerente, isolata e durevole (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: Che cos'è una transazione?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a21eaec081a42e1cd4bcd60cb7cf48d609075eec772ed18fd41494c47d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289721"
---
# <a name="what-is-a-transaction"></a>Che cos'è una transazione?

Una transazione è un gruppo di operazioni con le proprietà seguenti: atomica, coerente, isolata e durevole (ACID). Il supporto delle transazioni consente di sviluppare nuovi tipi di applicazioni, semplificando al tempo stesso il processo di sviluppo e rendendo l'applicazione più affidabile. Nella parte restante di questo argomento vengono forniti scenari che illustrano la necessità di queste proprietà, quindi una tabella che definisce ogni proprietà.

In un *gruppo atomico* di operazioni, ogni operazione nel gruppo deve avere esito positivo o gli effetti di tutte le operazioni devono essere annullati (operazione nota anche come *rollback).* Ad esempio, un bonifico bancario deve essere un set atomico di due operazioni: un debito da un conto e un credito per un altro conto. Il debito e il credito devono essere implementati come gruppo atomico. Se queste due operazioni non hanno esito positivo, il trasferimento è equamente a favore della banca o del titolare del conto.

Il requisito di *coerenza* indica che i dati sono coerenti dopo la transazione (presupponendo che sia stato avviato un sistema coerente prima della transazione). Per l'esempio di trasferimento bancario, la coerenza può essere definita come costante se il saldo combinato dei due conti è costante. Per implementare la coerenza nell'esempio di trasferimento bancario, le operazioni di debito e credito devono essere semplicemente per la stessa quantità di denaro.

Un altro esempio di transazione è un aggiornamento di un sito Web. Un sito di e-commerce richiede che una nuova pagina di navigazione della categoria di prodotti venga visualizzata esattamente nello stesso momento delle pagine dei dettagli dei prodotti che descrivono i nuovi prodotti. In questo caso, è necessario aggiornare e aggiungere più voci di directory sotto il controllo di una transazione. Non solo è necessario che gli aggiornamenti siano atomici, ma è anche necessario che un cliente che attualmente fa acquisti non sia in grado di visualizzare gli aggiornamenti in corso. Di seguito è riportato un esempio della *proprietà di* isolamento delle transazioni.

La proprietà di *durabilità richiede* che al termine di un aggiornamento i relativi effetti permangono anche se il sistema smette di rispondere. Nell'esempio precedente, la durabilità può essere fornita semplicemente garantendo un ripristino dei dati adeguato in modo che tutte le nuove voci di file system che rappresentano l'aggiunta di un nuovo prodotto al sito vengano visualizzate dopo che un sistema smette di rispondere. Questa operazione richiede un sistema con meccanismi di backup, ripristino e disponibilità elevata dei dati.

La garanzia dell'atomicità di una transazione, nonché delle altre proprietà, è presente in caso di un numero qualsiasi di errori, inclusi quelli che si verificano durante la fase di recupero di un errore precedente. Alla fine il sistema raggiungerà uno dei due stati seguenti: tutte le operazioni sono state applicate o nessuna delle operazioni è stata applicata.

Le proprietà di una transazione sono riepilogate nella tabella seguente.



| Termine                                                                                                         | Descrizione                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomica<br/>                 | Tutte le operazioni nella transazione hanno esito positivo o nessuna delle operazioni viene mantenuta.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente<br/> | Se i dati sono coerenti prima dell'inizio della transazione, saranno coerenti al termine della transazione.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isolato <br/>     | Gli effetti di una transazione in corso sono nascosti a tutte le altre transazioni.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durevole<br/>             | Al termine di una transazione, i risultati sono persistenti e non si verificano più in caso di arresto anomalo del sistema.<br/>                               |



 

Queste proprietà assicurano che il software possa gestire errori imprevisti, perché può semplicemente interrompere una transazione quando una situazione imprevista impedisce il completamento corretto. L'infrastruttura delle transazioni garantisce che viene eseguito il rollback di tutti gli effetti della transazione interrotta, riportando i dati a uno stato coerente. Di conseguenza, un sistema transazionale consente un recupero senza problemi di sistema.

Per garantire le proprietà ACID, un sistema che supporta le transazioni deve avere una funzionalità di registrazione affidabile che può essere usata per eseguire il commit o il rollback delle transazioni in base alle esigenze. Per altre informazioni, vedere [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

