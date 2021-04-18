---
title: Considerazioni sui mercati internazionali
description: Considerazioni sui mercati internazionali
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Negozi online di Windows Media Player, mercati internazionali
- negozi online, mercati internazionali
- digitare 1 negozi online, mercati internazionali
- digitare 2 negozi online, mercati internazionali
- mercati internazionali
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298471"
---
# <a name="considerations-for-international-markets"></a>Considerazioni sui mercati internazionali

Se la società crea negozi online per più mercati, è necessario fornire a Microsoft l'URL di un documento ServiceInfo per ogni mercato. Questa operazione può essere eseguita in uno dei due modi seguenti:

-   Creare un documento ServiceInfo separato per ogni mercato. In questo caso, è possibile fornire a Microsoft URL che puntano a singoli documenti ServiceInfo per ogni negozio online in ogni mercato.
-   Creare un singolo documento ServiceInfo per tutti i mercati. Quando si esegue questa operazione, si fornisce a Microsoft lo stesso URL per ogni mercato. Il documento ServiceInfo, creato come pagina ASP, può quindi rilevare dinamicamente la posizione dell'utente in base ai parametri della stringa di query.

Windows Media Player aggiunge una stringa di query alla richiesta dell'URL ServiceInfo che fornisce informazioni sulle impostazioni locali e sulla posizione dell'utente. Se il negozio online usa queste informazioni per determinare il contenuto da visualizzare, è necessario aggiungere i valori in modo dinamico ai propri URL nel documento ServiceInfo. Questo è il modo migliore per assicurarsi che gli URL delle pagine Web contengano sempre i parametri previsti.

Dopo aver determinato la posizione e la preferenza per la lingua dell'utente, è possibile salvare in modo permanente le informazioni per le sessioni future. A tale scopo, è possibile usare qualsiasi tecnica utilizzata in genere in una pagina Web, ad esempio cookie, oppure usando l'oggetto COM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




