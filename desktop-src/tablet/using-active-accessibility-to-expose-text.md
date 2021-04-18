---
description: Panoramica dell'utilizzo di Active Accessibility per esporre il testo.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Utilizzo di Active Accessibility per esporre il testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306723"
---
# <a name="using-active-accessibility-to-expose-text"></a>Utilizzo di Active Accessibility per esporre il testo

Le applicazioni possono utilizzare Microsoft Active Accessibility per esporre il testo. Tuttavia, l'interfaccia [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definita da versioni precedenti di Active Accessibility non è ottimizzata per l'esposizione di grandi quantità di testo RTF. Le versioni successive definiscono le interfacce ottimizzate per esporre grandi quantità di testo e attributi testuali.

Per esporre il testo di grandi quantità, creare oggetti Component Object Model (COM) distinti che supportano [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), o elementi figlio, per rappresentare ogni esecuzione di testo. Un'esecuzione è una riga, o parte di una linea, che condivide la stessa formattazione.

Active Accessibility espone solo il testo e il relativo percorso, ma non ha alcun meccanismo per esporre la formattazione del testo. Nonostante queste limitazioni, alcuni programmi utilizzano Active Accessibility per esporre il testo. Ad esempio, Microsoft Internet Explorer e Microsoft Visual Studio utilizzano entrambi Active Accessibility per esporre grandi quantità di testo.

Per ulteriori informazioni sull'esposizione del testo tramite Active Accessibility, vedere [accessibilità](../accessibility/accessibility.md).

 

 
