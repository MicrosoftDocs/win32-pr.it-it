---
description: In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo per organizzare elementi quali file, posta elettronica o contatti.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementazione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232521"
---
# <a name="implementing-property-handlers"></a>Implementazione di gestori di proprietà

In Windows Vista e versioni successive, i metadati sono diventati centrali come metodo per organizzare elementi quali file, posta elettronica o contatti. Per abilitare un sistema in cui è possibile eseguire la ricerca di elementi in base ai relativi metadati e dove gli utenti possono leggere o scrivere i metadati, Windows Vista ha introdotto un nuovo sistema di proprietà. I metadati in questo sistema sono rappresentati da un set estendibile di proprietà. In questo set di argomenti viene descritto come creare un gestore che legge e scrive le proprietà in e da un flusso di file. Questi gestori sono denominati gestori di proprietà e ognuno è associato a un determinato tipo di file, identificato dall'estensione del nome file.

Negli argomenti seguenti vengono illustrati i requisiti e le strategie necessari per la definizione delle proprietà e dei gestori di proprietà.

-   [Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
-   [Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
-   [Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
-   [Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
-   [Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
-   [Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di proprietà personalizzate.](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Schema Descrizione proprietà](./propdesc-schema-entry.md)
</dt> </dl>

 

 
