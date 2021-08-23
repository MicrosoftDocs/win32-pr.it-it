---
description: 'Altre informazioni su: Indicizzazione nella tabella'
title: Indicizzazione nella tabella
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721451"
---
# <a name="indexing-in-the-table"></a>Indicizzazione nella tabella


_**Si applica a:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indicizzazione nella tabella

Un indice è un set di colonne chiave che definiscono un ordinamento permanente dei record in una tabella. I record sono voci di indice nell'indice primario. È possibile definire un indice primario e più indici secondari per creare ordini di dati diversi nella tabella.

Anche se è possibile definire più indici, i record vengono archiviati fisicamente negli alberi B+ nell'ordine specificato dall'indice primario. L'indice primario è sempre un indice cluster e deve essere univoco. L'indice primario deve essere dichiarato prima dell'aggiornamento della prima tabella per mantenere l'ordinamento dell'indice. Quando l'applicazione non ha definito alcun indice primario, i dati vengono archiviati nell'ordine in cui i record vengono aggiunti alla tabella. Questo indice speciale viene definito indice sequenziale.

Gli alberi B+ separati vengono usati per ordinare i record in base all'indice secondario. Le voci di indice nell'indice secondario contengono puntatori ai dati archiviati in base all'indice primario. Le voci di indice per i record nell'indice primario devono essere univoche perché l'indice secondario punta al record usando la chiave primaria del record. Gli indici secondari possono avere o meno un vincolo di univocità. Per altre informazioni, vedere [l'argomento Panoramica del](./database-overview.md) database.
