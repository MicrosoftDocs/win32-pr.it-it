---
description: Perché è necessario Visualizzazione Compatibilità?
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Perché è necessario Visualizzazione Compatibilità?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5653ae72b3cbf3c21bd2458c1561c1d8823f2b883711e2c3890c16f792254b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328660"
---
# <a name="why-do-you-need-compatibility-view"></a>Perché è necessario Visualizzazione Compatibilità?

La Visualizzazione Compatibilità segue un set di regole per visualizzare correttamente il contenuto, senza alcuna azione dell'utente (o dell'amministratore IT) necessaria quando possibile. Visualizzazione Compatibilità consente agli sviluppatori di indicare al browser quale motore di rendering usare e consente agli utenti di eseguire l'override delle modalità di scelta e di cambio del browser. Se lo sviluppatore e il professionista IT non specificano la modalità di rendering da usare, l'utente visualizza l'icona "pagina interrotta" all'estremità destra della barra degli indirizzi, come illustrato nella figura seguente.

![illustrazione dell'icona della pagina interrotta accanto alla barra degli indirizzi](images/iecompatview.png)

Se un utente fa clic sull'icona, Windows Internet Explorer 8 cambia modalità di rendering e la pagina viene ricaricata immediatamente.

Gli utenti non visualizzano sempre questa icona. Si tratta di una soluzione secondaria anziché del meccanismo principale di compatibilità delle applicazioni. Windows Internet Explorer questa icona viene visualizzata solo quando una modifica in Visualizzazione Compatibilità ha senso, ad esempio quando un utente visualizza le pagine in modalità standard. In tutti gli altri casi, ad esempio quando un utente visualizza pagine in modalità non interattiva o visualizza siti dell'area Intranet, l'icona non viene visualizzata. Per altre informazioni sui Visualizzazione Compatibilità e su quando viene visualizzata l'icona, vedere [Introduzione Visualizzazione Compatibilità](/archive/blogs/ie/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
