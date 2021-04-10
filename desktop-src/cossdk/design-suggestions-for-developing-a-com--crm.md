---
description: Suggerimenti di progettazione per lo sviluppo di un CRM COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Suggerimenti di progettazione per lo sviluppo di un CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dcdb59f0ea23fb6879300d0bacec7df12970d81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225638"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Suggerimenti di progettazione per lo sviluppo di un CRM COM+

Di seguito sono riportati i passaggi consigliati per lo sviluppo di un CRM COM+:

1.  Prima di iniziare lo sviluppo, impostare il timeout della transazione su zero (utilizzando lo strumento di amministrazione Servizi componenti). Impostare il flag del registro di sistema VTRACE1 (vedere [impostazioni del registro di sistema com+ CRM](com--crm-registry-settings.md)) per visualizzare i messaggi di avviso e di errore di CRM nella traccia di debug.
2.  Determinare quale set di interfacce è necessario usare, strutturato (varianti) o non strutturato. (Vedere [interfacce com+ CRM](com--crm-interfaces.md)). Questo dipende dal linguaggio usato per sviluppare il CRM, ad esempio Microsoft Visual C++ o Microsoft Visual Basic.
3.  Sviluppare prima di tutto il ruolo di lavoro CRM. Determinare le informazioni necessarie nei record di log. Definire i tipi di record di log necessari e il relativo formato.
4.  Un compensatore CRM di debug viene fornito come parte degli esempi di CRM (nella Windows SDK). Questa operazione può essere utilizzata temporaneamente durante il debug del processo di lavoro CRM al posto del compensatore CRM reale.
5.  Quando il ruolo di lavoro CRM funziona correttamente, sviluppare il compensatore CRM reale e sostituire il compensatore CRM di debug con il compensatore CRM reale.
6.  Potrebbe essere auspicabile testare inizialmente il caso di ripristino. In tal caso, eliminare ogni volta il file di log CRM per l'applicazione server CRM prima di avviare l'applicazione server CRM.

## <a name="considerations"></a>Considerazioni

1.  **Scrivi avanti.** Il componente Worker CRM deve scrivere in anticipo; ovvero deve scrivere un record di log indicante che verrà eseguita un'azione prima di eseguire effettivamente tale azione. Inoltre, questo record di log deve essere forzato su disco dopo la scrittura e prima che venga eseguita l'azione.
2.  **Isolamento.** Il CRM non impone l'isolamento. La progettazione di CRM deve fornire l'isolamento tra più client in transazioni separate e deve considerare anche il caso prima del ripristino.
3.  **Ripristino in corso.** Il ruolo di lavoro CRM deve gestire il codice di errore "ripristino in corso". Per ulteriori informazioni su questo codice di errore, vedere [risoluzione dei problemi di com+ CRM](troubleshooting-the-com--crm.md) .
4.  **Gestione degli errori.** Il ruolo di lavoro CRM deve far fronte al caso in cui la transazione venga interrotta prima del previsto. Vedere la sezione [gestione degli errori in com+ CRM](error-handling-in-the-com--crm.md).
5.  **Tempo di ripristino.** Il compensatore CRM deve essere progettato per eseguire rapidamente il ripristino, in modo che non sia necessario attendere un nuovo lavoro per l'applicazione server CRM.
6.  **L'idempotenza.** È possibile che un compensatore CRM possa ricevere nuovamente lo stesso record di log, per annullare o ripristinare un'azione che è già stata annullata o ripetuta. Le azioni che il compensatore CRM può eseguire devono essere idempotente, che spesso significa che i codici di errore restituiti da queste azioni devono essere ignorati.
7.  **Avvio del ripristino.** Il ripristino di un'applicazione server CRM viene eseguito all'avvio dell'applicazione server CRM. Tuttavia, non è presente alcun avvio automatico di un'applicazione server CRM. Lo sviluppatore di applicazioni deve considerare la modalità di avvio di avvio e ripristino.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



