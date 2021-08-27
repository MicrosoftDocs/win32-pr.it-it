---
description: Le finestre di stato, composizione e candidati formano l'interfaccia utente per l'IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Stato, composizione e Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f5c385c14cd265630de77352e12e4c63bce806837462f3c9ab3c204940e66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130111"
---
# <a name="status-composition-and-candidates-windows"></a>Stato, composizione e Windows

Le finestre di stato, composizione e candidati formano l'interfaccia utente per l'IME. La finestra di stato indica che l'IME è aperto e fornisce all'utente i mezzi per impostare le modalità di conversione. La finestra di composizione viene visualizzata quando l'utente immette testo e, a seconda della modalità di conversione, visualizza il testo come immesso o visualizza il testo convertito. La finestra dei candidati viene visualizzata insieme alla finestra di composizione. Contiene un elenco di "candidati" (caratteri alternativi) per il carattere o i caratteri selezionati nella finestra di composizione. L'utente può scorrere l'elenco dei candidati e selezionare i caratteri desiderati, quindi tornare alla finestra di composizione. L'utente può comporre il testo desiderato in questo modo fino a quando la stringa di composizione non viene finalizzata e la finestra viene chiusa.

L'IME invia i caratteri composti all'applicazione in grado di riconoscere IME sotto forma di messaggi [**WM \_ IME \_ CHAR**](wm-ime-char.md) o [**WM \_ IME \_ COMPOSITION**](wm-ime-composition.md)/GCS \_ RESULT. Se l'applicazione non elabora questi messaggi, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) li converte in uno o più [**messaggi WM \_ CHAR.**](../inputdev/wm-char.md)

Per impostazione predefinita, il sistema operativo crea e gestisce automaticamente le finestre di stato, composizione e candidati per i requisiti di input di testo. Per molte applicazioni, questa elaborazione predefinita è sufficiente. Queste applicazioni si basano interamente sul sistema operativo per il supporto IME e vengono detto "IME non consapevoli" perché non sono a conoscenza delle numerose attività eseguite dal sistema operativo per gestire le finestre IME.

Un'applicazione in grado di riconoscere IME, d'altra parte, partecipa alla creazione e alla gestione delle finestre IME. Tali applicazioni controllano l'operazione, la posizione e l'aspetto delle finestre predefinite inviando messaggi a queste finestre e intercettando ed elaborando i messaggi dalle finestre. In alcuni casi, le applicazioni creano le proprie finestre IME e forniscono l'elaborazione completa per le finestre di stato, composizione e candidati personalizzate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
