---
description: La procedura seguente descrive uno scenario per generare una trasformazione che nasconde in modo permanente una funzionalità.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generazione di una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635989"
---
# <a name="generating-a-transform"></a>Generazione di una trasformazione

La procedura seguente descrive uno scenario per generare una trasformazione che nasconde in modo permanente una funzionalità.

**Per nascondere in modo permanente una funzionalità del prodotto**

1.  Copiare il pacchetto di installazione originale.
2.  Modificare la copia impostando il valore della colonna Display nella [tabella Feature su](feature-table.md) zero. Specifica di nascondere la funzionalità.
3.  Creare una trasformazione dal pacchetto di installazione originale ai nuovi pacchetti di installazione chiamando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Creare le informazioni di riepilogo nella trasformazione chiamando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La trasformazione è quindi pronta per l'applicazione durante l'installazione. Per altre informazioni, vedere [Applicazione di trasformazioni](applying-transforms.md).

 

 



