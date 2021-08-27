---
title: Funzioni del contesto di interazione
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni del contesto di interazione.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
- mouse
- penna
- stilo
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758337"
---
# <a name="interaction-context-functions"></a>Funzioni del contesto di interazione

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [funzioni del contesto di](interaction-context-portal.md) interazione.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Includere il puntatore specificato nel set di puntatori elaborati [dall'oggetto contesto di](interaction-context-portal.md) interazione. <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Aggiunge la cronologia per un singolo puntatore di input al buffer [dell'oggetto Contesto interazione.](interaction-context-portal.md)<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Crea e inizializza un oggetto [contesto di](interaction-context-portal.md) interazione.<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Elimina l'oggetto [contesto di interazione](interaction-context-portal.md) specificato.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Ottiene il comportamento di interazione tramite scorrimento incrociato. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Ottiene il comportamento di inerzia di una manipolazione (traslazione, rotazione, ridimensionamento). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Ottiene lo stato di configurazione dell'interazione per [l'oggetto contesto di](interaction-context-portal.md) interazione.<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Ottiene lo stato della rotellina del mouse per [l'oggetto contesto di](interaction-context-portal.md) interazione. <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Ottiene le [proprietà dell'oggetto contesto](interaction-context-portal.md) di interazione.<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Ottiene lo [stato corrente del contesto](interaction-context-portal.md) di interazione e l'ora in cui il contesto torna allo stato inattivo. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Elaborare i pacchetti memorizzati nel buffer alla fine di un frame di input del puntatore.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Invia l'input del timer [all'oggetto contesto di](interaction-context-portal.md) interazione per l'elaborazione dell'inerzia.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Elabora un set di frame di input del puntatore.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registra un callback per ricevere eventi di interazione da un [oggetto contesto di](interaction-context-portal.md) interazione.<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Rimuovere il puntatore specificato dal set di puntatori elaborati [dall'oggetto contesto di](interaction-context-portal.md) interazione. <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Reimposta lo stato [**di interazione,**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state)le impostazioni di configurazione dell'interazione e tutti i parametri allo stato iniziale. Le interazioni correnti vengono annullate senza notifiche. <br/> [Il contesto di](interaction-context-portal.md) interazione deve essere riconfigurato prima dell'uso successivo.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configura l'interazione tra scorrimenti. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configura il comportamento di inerzia di una manipolazione (traslazione, rotazione, ridimensionamento) dopo l'elevamento del contatto. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configura [l'oggetto contesto di](interaction-context-portal.md) interazione per elaborare le modifiche specificate.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Imposta i valori dei parametri per l'input della rotellina del mouse. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Imposta il punto centrale e il raggio del pivot dal punto centrale per una manipolazione di rotazione usando un singolo puntatore di input. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Imposta le [proprietà dell'oggetto Contesto](interaction-context-portal.md) di interazione.<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Imposta lo stato [**di interazione su**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) INTERACTION STATE IDLE e lascia intatte tutte le impostazioni e i parametri di configurazione \_ \_ dell'interazione. Le interazioni correnti vengono annullate e le notifiche vengono inviate in base alle esigenze.<br/> [Il contesto](interaction-context-portal.md) di interazione non deve essere riconfigurato prima dell'uso successivo.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Informazioni di riferimento sul contesto di interazione](interaction-context-reference.md)
