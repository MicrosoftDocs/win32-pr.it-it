---
description: Tabelle Frequency
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tabelle Frequency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123561"
---
# <a name="frequency-tables"></a>Tabelle Frequency

Il filtro del sintonizzatore TV (kstvtune.ax) include un elenco interno di tabelle di frequenza. Ogni tabella Frequency contiene un elenco di frequenze e corrisponde alle frequenze broadcast o Cable per un determinato paese/area geografica. Un'applicazione viene ottimizzata per una determinata frequenza chiamando il metodo [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con l'indice della frequenza desiderata.

Per alcuni paesi o aree geografiche, i numeri di indice delle tabelle di frequenza vengono mappati direttamente ai numeri di canale. Tuttavia, i numeri di canale fissi non sono appropriati per tutti i mercati. Ad esempio, i numeri di canale europei non vengono effettivamente utilizzati dai consumer. Al contrario, gli utenti si aspettano di scegliere e assegnare i propri numeri di canale per le frequenze usate dagli operatori broadcast o Cable nell'area. Per questi paesi/aree geografiche, le applicazioni non devono esporre i numeri di indice direttamente all'utente. Instread, l'applicazione deve tenere un mapping interno tra i numeri di canale (presentati all'utente) e gli indici di frequenza (per l'ottimizzazione).

La maggior parte degli operatori di cavi non statunitensi è gratuita per la trasmissione in base alle frequenze scelte, spesso combinando frequenze da standard diversi nella stessa linea di canali. Viene quindi usata una tabella con frequenza "Unicable" per qualsiasi paese/area geografica priva di standard Cable Channel standard Authority. Viene inoltre fornito un meccanismo per eseguire l'override delle singole frequenze nelle tabelle di frequenza. Questo meccanismo è descritto nella sezione seguente, [sostituzioni di frequenza](frequency-overrides.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione della TV analoga internazionale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



