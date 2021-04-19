---
description: .
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Perché è necessaria la visualizzazione compatibilità?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fd1902ad77af863e61be36800a8c4f9eabf227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318569"
---
# <a name="why-do-you-need-compatibility-view"></a>Perché è necessaria la visualizzazione compatibilità?

La funzionalità Visualizzazione compatibilità segue un set di regole per visualizzare correttamente il contenuto, senza l'intervento dell'utente o dell'amministratore IT necessario laddove possibile. La visualizzazione compatibilità consente agli sviluppatori di indicare al browser quale motore di rendering utilizzare e consente agli utenti di eseguire l'override delle modalità scelta e switch del browser. Se lo sviluppatore e i professionisti IT non specificano la modalità di rendering da usare, l'utente Visualizza l'icona "pagina interrotta" all'estremità destra della barra degli indirizzi, come illustrato nella figura seguente.

![illustrazione dell'icona di pagina interrotta accanto alla barra degli indirizzi](images/iecompatview.png)

Se un utente fa clic sull'icona, Windows Internet Explorer 8 passa le modalità di rendering e la pagina viene ricaricata immediatamente.

Questa icona non viene sempre visualizzata dagli utenti. Si tratta di una soluzione secondaria anziché del meccanismo primario di compatibilità delle applicazioni. In Windows Internet Explorer questa icona viene visualizzata solo quando è opportuno modificare la visualizzazione compatibilità, ad esempio quando un utente visualizza le pagine della modalità standard. In tutti gli altri casi, ad esempio quando un utente visualizza le pagine della modalità non standard o Visualizza i siti dell'area Intranet, l'icona non viene visualizzata. Per ulteriori informazioni sulla visualizzazione compatibilità e sul momento in cui viene visualizzata l'icona, vedere [Introduzione alla visualizzazione compatibilità](/archive/blogs/ie/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
