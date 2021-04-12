---
description: Le finestre stato, composizione e candidati formano l'interfaccia utente per l'IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Finestre stato, composizione e candidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b800def67299a464fd232a08a2bbff0a2a60a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234047"
---
# <a name="status-composition-and-candidates-windows"></a>Finestre stato, composizione e candidati

Le finestre stato, composizione e candidati formano l'interfaccia utente per l'IME. La finestra di stato indica che l'IME è aperto e fornisce all'utente i mezzi per impostare le modalità di conversione. La finestra di composizione viene visualizzata quando l'utente immette il testo e, a seconda della modalità di conversione, Visualizza il testo come immesso o Visualizza il testo convertito. La finestra candidati viene visualizzata insieme alla finestra di composizione. Contiene un elenco di "candidati" (caratteri alternativi) per il carattere o i caratteri selezionati nella finestra di composizione. L'utente può scorrere l'elenco dei candidati e selezionare i caratteri desiderati, quindi tornare alla finestra di composizione. L'utente può comporre il testo desiderato in questo modo fino alla finalizzazione della stringa di composizione e alla chiusura della finestra.

L'IME invia i caratteri composti all'applicazione in grado di riconoscere IME sotto forma di messaggi di risultato/GCS di [**WM \_ IME \_ char**](wm-ime-char.md) o [**WM \_ IME \_ Composition**](wm-ime-composition.md) \_ . Se l'applicazione non elabora questi messaggi, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) li converte in uno o più messaggi [**WM \_ char**](../inputdev/wm-char.md) .

Per impostazione predefinita, il sistema operativo crea e gestisce automaticamente le finestre stato, composizione e candidati per i requisiti di input di testo. Per molte applicazioni, questa elaborazione predefinita è sufficiente. Queste applicazioni si basano interamente sul sistema operativo per il supporto IME e sono dette "non compatibili con IME" perché non sono consapevoli delle numerose attività eseguite dal sistema operativo per gestire le finestre IME.

Un'applicazione in grado di riconoscere gli IME, d'altra parte, partecipa alla creazione e alla gestione delle finestre IME. Tali applicazioni controllano l'operazione, la posizione e l'aspetto delle finestre predefinite inviando messaggi a queste finestre e intercettando ed elaborando i messaggi da Windows. In alcuni casi, le applicazioni creano le proprie finestre IME e forniscono l'elaborazione completa per le finestre di stato, composizione e candidati personalizzate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione metodi di input](about-input-method-manager.md)
</dt> </dl>

 

 
