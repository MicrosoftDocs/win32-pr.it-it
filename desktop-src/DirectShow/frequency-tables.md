---
description: Tabelle di frequenza
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tabelle di frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db832144aedb8f64d18692a30a8e8c7d812c4cbd517b1b9ab31bd9cdc231019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401259"
---
# <a name="frequency-tables"></a>Tabelle di frequenza

Il filtro Siner TV (kstvtune.ax) include un elenco interno di tabelle di frequenza. Ogni tabella delle frequenze contiene un elenco di frequenze e corrisponde alle frequenze di trasmissione o cavo per un determinato paese/area geografica. Un'applicazione esegue l'aggiornamento a una determinata frequenza chiamando il metodo [**IAMTuner::p ut \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con l'indice della frequenza desiderata.

Per alcuni paesi/aree geografiche, i numeri di indice delle tabelle di frequenza vengono mappati direttamente ai numeri di canale. I numeri di canale fissi non sono tuttavia appropriati per tutti i mercati. Ad esempio, i numeri di canale europei non vengono effettivamente usati dai consumer. Al contrario, i consumer si aspettano di scegliere e assegnare i propri numeri di canale per le frequenze usate dagli operatori broadcast o via cavo nella propria area. Per questi paesi/aree geografiche, le applicazioni non devono esporre i numeri di indice direttamente all'utente. Instread, l'applicazione deve mantenere un mapping interno tra i numeri di canale (presentati all'utente) e gli indici di frequenza (per l'ottimizzazione).

La maggior parte degli operatori di cavi non statunitensi è gratuita per la trasmissione su frequenze di propria scelta, spesso combinando frequenze di standard diversi nella stessa linea di canali. Di conseguenza, viene usata una tabella di frequenza "Unicable" per qualsiasi paese/area geografica che non dispone di un'autorità standard per gli standard del canale via cavo. Viene inoltre fornito un meccanismo per eseguire l'override delle singole frequenze nelle tabelle delle frequenze. Questo meccanismo è descritto nella sezione seguente, [Sostituzioni di frequenza](frequency-overrides.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione tv analogica internazionale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



