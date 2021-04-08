---
title: Indicatori
description: Indicatori
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcatori
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- marcatori, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856893"
---
# <a name="markers"></a>Indicatori

I marcatori sono posizioni denominate nella sequenza temporale di un file ASF. Ogni marcatore ha un nome e un'ora di presentazione assegnata. È possibile specificare tutti i marcatori necessari per un file.

I marcatori sono utili per suddividere i file ASF di grandi dimensioni in parti logiche. Un'applicazione che utilizza l'oggetto Reader per riprodurre file ASF può fornire all'utente la possibilità di passare dal marcatore al marcatore, semplificando la navigazione dei supporti digitali. Se, ad esempio, si crea un file ASF da una presentazione, è possibile inserire i marcatori nella sequenza temporale per ogni argomento principale descritto. Al momento della riproduzione, anziché ottenere una sequenza temporale molto estesa e dover indovinare la posizione in cui eseguire la ricerca, un utente può semplicemente selezionare un argomento da un elenco e passare direttamente alla parte pertinente del file.

I marcatori vengono modificati dall'oggetto dell'editor di metadati. È possibile aggiungere, rimuovere e visualizzare i marcatori in un file in qualsiasi momento dopo la scrittura del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Per cercare i marcatori**](to-seek-to-markers.md)
</dt> <dt>

[**Uso dei marcatori**](using-markers.md)
</dt> </dl>

 

 




