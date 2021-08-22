---
description: Panoramica dell'uso dell'accessibilità attiva per esporre il testo.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Uso Active Accessibility per esporre testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 247d78149b82d15eb7c2dbd4ac2b2463d53c5d454dcb7877906197661de36ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334791"
---
# <a name="using-active-accessibility-to-expose-text"></a>Uso Active Accessibility per esporre testo

Le applicazioni possono usare Microsoft Active Accessibility per esporre il testo. Tuttavia, [**l'interfaccia IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definita dalle versioni precedenti Active Accessibility non è ottimizzata per l'esposizione di grandi quantità di testo RTF. Le versioni successive definiscono interfacce ottimizzate per l'esposizione di grandi quantità di attributi di testo e testuali.

Per esporre testo di grandi dimensioni, creare oggetti COMPONENT OBJECT MODEL (COM) separati che supportano [**elementi IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)o figlio, per rappresentare ogni esecuzione di testo. Un'esecuzione è una riga, o parte di una riga, che condivide la stessa formattazione.

Active Accessibility espone solo il testo e la relativa posizione, ma non ha alcun meccanismo per esporre la formattazione del testo. Nonostante queste limitazioni, alcuni programmi usano Active Accessibility per esporre il testo. Ad esempio, Microsoft Internet Explorer e Microsoft Visual Studio usano entrambi Active Accessibility per esporre grandi quantità di testo.

Per altre informazioni sull'esposizione di testo usando Active Accessibility, vedere [Accessibilità](../accessibility/accessibility.md).

 

 
