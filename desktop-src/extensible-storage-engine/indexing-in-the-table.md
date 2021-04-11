---
description: 'Altre informazioni su: indicizzazione nella tabella'
title: Indicizzazione nella tabella
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049611"
---
# <a name="indexing-in-the-table"></a>Indicizzazione nella tabella


_**Si applica a:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indicizzazione nella tabella

Un indice è un set di colonne chiave che definiscono un ordinamento permanente dei record in una tabella. I record sono voci di indice nell'indice primario. È possibile definire un indice primario e più indici secondari per creare ordini diversi di dati nella tabella.

Sebbene sia possibile definire più indici, i record vengono archiviati fisicamente in alberi B + nell'ordine specificato dall'indice primario. L'indice primario è sempre un indice cluster e deve anche essere univoco. L'indice primario deve essere dichiarato prima dell'aggiornamento della prima tabella per mantenere l'ordine degli indici. Quando l'applicazione non definisce alcun indice primario, i dati vengono archiviati nell'ordine in cui i record vengono aggiunti alla tabella. Questo indice speciale viene definito indice sequenziale.

Gli alberi B + separati vengono usati per ordinare i record in base all'indice secondario. Le voci di indice nell'indice secondario contengono puntatori ai dati archiviati in base all'indice primario. Le voci di indice per i record nell'indice primario devono essere univoche perché l'indice secondario punta al record utilizzando la chiave primaria del record. Gli indici secondari possono avere o meno un vincolo di univocità. Per ulteriori informazioni, vedere l'argomento relativo alla [Panoramica del database](./database-overview.md) .
