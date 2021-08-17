---
description: Informazioni su come creare un gestore delle proprietà che legge e scrive le proprietà in e da un flusso di file. Ogni gestore è associato a un determinato tipo di file.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementazione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df4012168a0b6d1af5db727907e1c0fdc07231eac42abfbd3b96e8daab2f3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469127"
---
# <a name="implementing-property-handlers"></a>Implementazione di gestori di proprietà

In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo di organizzazione di elementi come file, messaggi di posta elettronica o contatti. Per abilitare un sistema in cui è possibile eseguire ricerche di elementi in base ai relativi metadati e in cui gli utenti possono leggere o scrivere i metadati, Windows Vista ha introdotto un nuovo sistema di proprietà. I metadati in questo sistema sono rappresentati da un set estendibile di proprietà. In questo set di argomenti viene descritto come creare un gestore che legge e scrive le proprietà in e da un flusso di file. Questi gestori sono denominati gestori di proprietà e ognuno è associato a un determinato tipo di file, identificato dall'estensione del nome file.

Negli argomenti seguenti vengono illustrati i requisiti e le strategie necessari per definire le proprietà e i gestori delle proprietà.

-   [Informazioni sui gestori di proprietà](./building-property-handlers-properties.md)
-   [Uso di nomi di tipi](./building-property-handlers-user-friendly-kind-names.md)
-   [Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
-   [Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
-   [Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
-   [Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di proprietà personalizzate.](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Schema di descrizione delle proprietà](./propdesc-schema-entry.md)
</dt> </dl>

 

 
