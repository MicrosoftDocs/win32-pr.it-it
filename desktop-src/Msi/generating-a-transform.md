---
description: Nella procedura riportata di seguito viene descritto uno scenario per generare una trasformazione che nasconde una funzionalità in modo permanente.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generazione di una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057813"
---
# <a name="generating-a-transform"></a>Generazione di una trasformazione

Nella procedura riportata di seguito viene descritto uno scenario per generare una trasformazione che nasconde una funzionalità in modo permanente.

**Per nascondere in modo permanente una funzionalità del prodotto**

1.  Copiare il pacchetto di installazione originale.
2.  Modificare la copia impostando il valore della colonna di visualizzazione nella [tabella delle funzionalità](feature-table.md) su zero. Consente di specificare di nascondere la funzionalità.
3.  Creare una trasformazione dal pacchetto di installazione originale nei nuovi pacchetti di installazione chiamando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Creare le informazioni di riepilogo nella trasformazione chiamando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

La trasformazione sarà quindi pronta per essere applicata durante l'installazione. Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).

 

 



