---
title: Considerazioni per i mercati internazionali
description: Considerazioni per i mercati internazionali
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player negozi online, mercati internazionali
- negozi online, mercati internazionali
- negozi online di tipo 1, mercati internazionali
- negozi online di tipo 2, mercati internazionali
- mercati internazionali
- Windows Media Player negozi online, documento ServiceInfo
- negozi online, documento ServiceInfo
- tipo 1 negozi online, documento ServiceInfo
- Tipo 2 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580511"
---
# <a name="considerations-for-international-markets"></a>Considerazioni per i mercati internazionali

Se l'azienda crea negozi online per più mercati, è necessario fornire a Microsoft l'URL di un documento ServiceInfo per ogni mercato. È possibile eseguire questa operazione in uno dei due modi seguenti:

-   Creare un documento ServiceInfo separato per ogni mercato. In questo caso, si forniscono a Microsoft URL che puntano a singoli documenti ServiceInfo per ogni negozio online in ogni mercato.
-   Creare un singolo documento ServiceInfo per tutti i mercati. In questo caso, si fornisce a Microsoft lo stesso URL per ogni mercato. Il documento ServiceInfo, creato come pagina ASP, può quindi rilevare dinamicamente la posizione dell'utente in base ai parametri della stringa di query.

Windows Media Player aggiunge una stringa di query alla richiesta URL ServiceInfo che fornisce informazioni sulle impostazioni locali e sulla posizione dell'utente. Se il negozio online usa queste informazioni per determinare il contenuto da visualizzare, è necessario aggiungere dinamicamente questi valori ai propri URL nel documento ServiceInfo. Questo è il modo migliore per garantire che gli URL della pagina Web contengano sempre i parametri previsti.

Dopo aver determinato la posizione e la preferenza di lingua dell'utente, è possibile rendere persistenti queste informazioni per le sessioni future. È possibile eseguire questa operazione usando una delle tecniche usate normalmente in una pagina Web, ad esempio i cookie, o usando l'oggetto COM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




