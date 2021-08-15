---
description: Suggerimenti di progettazione per lo sviluppo di un CRM COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Suggerimenti di progettazione per lo sviluppo di un CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128753"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Suggerimenti di progettazione per lo sviluppo di un CRM COM+

Di seguito sono riportati i passaggi consigliati per lo sviluppo di un CRM COM+:

1.  Prima di avviare lo sviluppo, impostare il timeout della transazione su zero (usando lo strumento di amministrazione Servizi componenti). Impostare il flag del Registro di sistema VTRACE1 (vedere [COM+ CRM Registry Impostazioni](com--crm-registry-settings.md)) per visualizzare i messaggi di avviso e di errore CRM nella traccia di debug.
2.  Determinare quale set di interfacce è necessario usare, strutturato (varianti) o non strutturato. Vedere [Interfacce CRM COM+.](com--crm-interfaces.md) Ciò dipende dal linguaggio utilizzato per sviluppare crm, ad esempio Microsoft Visual C++ o Microsoft Visual Basic.
3.  Sviluppare prima il ruolo di lavoro CRM. Determinare le informazioni necessarie nei record di log. Definire i tipi di record di log necessari e il relativo formato.
4.  Un compensatore CRM di debug viene fornito come parte degli esempi CRM (in Windows SDK). Può essere usato temporaneamente durante il debug del ruolo di lavoro CRM al posto del compensatore CRM reale.
5.  Quando il ruolo di lavoro CRM funziona correttamente, sviluppare il compensatore CRM reale e sostituire il compensatore CRM di debug con il compensatore CRM reale.
6.  Potrebbe essere preferibile non testare inizialmente il caso di ripristino. In tal caso, eliminare il file di log CRM per l'applicazione server CRM ogni volta prima di avviare l'applicazione server CRM.

## <a name="considerations"></a>Considerazioni

1.  **Scrivere in anticipo.** Il componente del ruolo di lavoro CRM deve scrivere in anticipo. in altre informazioni, deve scrivere un record di log che indica che eseguirà un'azione prima di eseguire effettivamente tale azione. Inoltre, questo record di log deve essere forzato su disco dopo la scrittura e prima che venga eseguita l'azione.
2.  **Isolamento.** Crm non impone l'isolamento. La progettazione CRM deve fornire l'isolamento tra più client in transazioni separate e deve considerare anche il caso prima del ripristino.
3.  **Ripristino in corso.** Il ruolo di lavoro CRM deve gestire il codice di errore "Ripristino in corso". Per altre informazioni su questo codice di errore, vedere Risoluzione dei problemi di [COM+ CRM.](troubleshooting-the-com--crm.md)
4.  **Gestione degli errori.** Il ruolo di lavoro CRM deve gestire il caso in cui la transazione viene interrotta prima del previsto. Vedere la sezione [Gestione degli errori in COM+ CRM.](error-handling-in-the-com--crm.md)
5.  **Tempo di ripristino.** Il compensatore CRM deve essere progettato per eseguire rapidamente il ripristino in modo che non sia necessario attendere il nuovo lavoro per l'applicazione server CRM.
6.  **Idempotenza.** È possibile che un compensatore CRM riceva nuovamente lo stesso record di log per annullare o ripetere un'azione che è già stata annullata o di cui è già stato annullato il nuovo record. Le azioni che il compensatore CRM potrebbe eseguire devono essere idempotenti, il che spesso significa che i codici di errore restituiti da queste azioni devono essere ignorati.
7.  **Avvio del ripristino.** Il ripristino di un'applicazione server CRM viene eseguito all'avvio dell'applicazione server CRM. Tuttavia, non è disponibile l'avvio automatico di un'applicazione server CRM. Lo sviluppatore dell'applicazione deve considerare come devono essere avviati sia l'avvio che il ripristino.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



