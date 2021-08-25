---
title: Marcatori
description: Marcatori
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows MEDIA Format SDK, marcatori
- Advanced Systems Format (ASF), marcatori
- ASF (Advanced Systems Format), marcatori
- marcatori, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58ddc013b2d8e09fa30ac6a8b7373aaf6733b669f2ccacec6350ee70e0800b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808231"
---
# <a name="markers"></a>Marcatori

I marcatori sono posizioni denominate nella sequenza temporale di un file ASF. Ogni marcatore ha un nome e un'ora di presentazione da assegnare. È possibile specificare il numero di marcatori necessario per un file.

I marcatori sono utili per suddividere file ASF di grandi dimensioni in parti logiche. Un'applicazione che usa l'oggetto lettore per riprodurre file ASF può fornire all'utente la possibilità di passare da marcatore a marcatore, semplificando la navigazione dei supporti digitali. Ad esempio, se si sta rendendo un file ASF da una presentazione, è possibile inserire marcatori nella sequenza temporale per ogni argomento principale illustrato. Durante la riproduzione, invece di ottenere una lunga sequenza temporale e dover indovinare la posizione in cui cercare, un utente può semplicemente selezionare un argomento da un elenco e passare direttamente alla parte pertinente del file.

I marcatori vengono manipolati dall'oggetto dell'editor di metadati. È possibile aggiungere, rimuovere e visualizzare i marcatori in un file in qualsiasi momento dopo la scrittura del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Per cercare marcatori**](to-seek-to-markers.md)
</dt> <dt>

[**Uso dei marcatori**](using-markers.md)
</dt> </dl>

 

 




