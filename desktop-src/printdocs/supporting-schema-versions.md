---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Supporto delle versioni dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d674449d581aca2ddfc80da2312b31eb6c930a6f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321035"
---
# <a name="supporting-schema-versions"></a>Supporto delle versioni dello schema

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il Framework dello schema di stampa è soggetto a modifiche in futuro quando si verificano nuove esigenze. Tali modifiche dovrebbero essere molto poco frequenti, perché la modifica più comune è l'introduzione di nuovi nomi di istanza. Questa modifica non influisce sulla struttura del Framework e deve essere trasparente per i client e i provider. Tutte le modifiche apportate alla struttura e all'organizzazione del Framework dello schema di stampa verranno identificate da incrementi al relativo numero di versione. Le aggiunte alle parole chiave dello schema di stampa non verranno identificate. I provider PrintTicket devono essere in grado di supportare la versione corrente di Print Schema Framework, nonché qualsiasi versione precedente. La versione di Print Schema Framework viene identificata utilizzando l'attributo XML: Version visualizzata in corrispondenza dell'elemento radice dell'oggetto PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



