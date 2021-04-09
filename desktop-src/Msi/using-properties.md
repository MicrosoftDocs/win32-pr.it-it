---
description: Nelle sezioni seguenti viene descritto l'utilizzo delle proprietà predefinite del programma di installazione e delle proprietà aggiuntive definite dall'autore del pacchetto.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Utilizzo delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129359"
---
# <a name="using-properties"></a>Utilizzo delle proprietà

Nelle sezioni seguenti viene descritto l'utilizzo delle proprietà predefinite del programma di installazione e delle proprietà aggiuntive definite dall'autore del pacchetto. Le proprietà possono essere proprietà [pubbliche](public-properties.md) o [proprietà private](private-properties.md). Ogni proprietà che deve essere definita al momento dell'inizializzazione del programma di installazione deve avere il nome e il valore iniziale elencati nella [tabella delle proprietà](property-table.md). Le proprietà con un valore null non sono elencate nella tabella delle proprietà. È possibile ottenere o impostare proprietà da programmi e azioni personalizzate e impostare proprietà pubbliche dalla riga di comando. Il processo di installazione può essere modificato usando le proprietà nelle istruzioni condizionali.

[Restrizioni per i nomi delle proprietà](restrictions-on-property-names.md)

[Inizializzazione dei valori delle proprietà](initialization-of-property-values.md)

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)

[Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md)

[Utilizzo di una proprietà di directory in un percorso](using-a-directory-property-in-a-path.md)

> [!Note]  
> Non usare le proprietà per le password o altre informazioni che devono rimanere sicure. Il programma di installazione può scrivere il valore di una proprietà creato nella tabella delle proprietà o creato in fase di esecuzione in un log o nel registro di sistema.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Riferimento alla proprietà](property-reference.md)
</dt> </dl>

 

 



