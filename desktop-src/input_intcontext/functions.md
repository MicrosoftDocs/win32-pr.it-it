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
ms.openlocfilehash: 7f57bf6ac2b5d9bc7f17a43cd84a6e8eb7d828a4
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/07/2020
ms.locfileid: "106299353"
---
# <a name="interaction-context-functions"></a>Funzioni del contesto di interazione

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni del [contesto di interazione](interaction-context-portal.md) .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Includere il puntatore specificato nel set di puntatori elaborati dall'oggetto [contesto di interazione](interaction-context-portal.md) . <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Aggiunge la cronologia per un singolo puntatore di input al buffer dell'oggetto [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Crea e Inizializza un oggetto del [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Elimina definitivamente l'oggetto [contesto di interazione](interaction-context-portal.md) specificato.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Ottiene il comportamento di interazione tra diapositive. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Ottiene il comportamento di inerzia di una manipolazione (traslazione, rotazione, ridimensionamento). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Ottiene lo stato di configurazione dell'interazione per l'oggetto [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Ottiene lo stato della rotellina del mouse per l'oggetto [contesto di interazione](interaction-context-portal.md) . <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Ottiene le proprietà dell'oggetto del [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Ottiene lo stato del [contesto di interazione](interaction-context-portal.md) corrente e l'ora in cui il contesto tornerà allo stato inattivo. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Elabora i pacchetti memorizzati nel buffer alla fine di un frame di input del puntatore.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Invia l'input del timer all'oggetto [contesto di interazione](interaction-context-portal.md) per l'elaborazione dell'inerzia.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Elabora un set di frame di input del puntatore.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registra un callback per ricevere eventi di interazione da un oggetto del [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Rimuovere il puntatore specificato dal set di puntatori elaborati dall'oggetto del [contesto di interazione](interaction-context-portal.md) . <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Reimposta lo stato di [**interazione**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), le impostazioni di configurazione dell'interazione e tutti i parametri sullo stato iniziale. Le interazioni correnti vengono annullate senza notifiche. <br/> È necessario riconfigurare il [contesto di interazione](interaction-context-portal.md) prima del successivo utilizzo.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configura l'interazione tra le diapositive. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configura il comportamento di inerzia di una manipolazione (traslazione, rotazione, ridimensionamento) dopo che il contatto è stato rimosso. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configura l'oggetto [contesto di interazione](interaction-context-portal.md) per elaborare le modifiche specificate.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Imposta i valori di parametro per l'input della rotellina del mouse. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Imposta il punto centrale e il raggio perno dal punto centrale, per una manipolazione della rotazione usando un singolo puntatore di input. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Imposta le proprietà dell'oggetto del [contesto di interazione](interaction-context-portal.md) .<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Imposta lo [**stato di interazione**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) sullo \_ stato di interazione \_ inattivo e lascia intatti tutti i parametri e le impostazioni di configurazione dell'interazione. Le interazioni correnti vengono annullate e le notifiche vengono inviate come richiesto.<br/> Non è necessario riconfigurare il [contesto di interazione](interaction-context-portal.md) prima del successivo utilizzo.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Riferimento al contesto di interazione](interaction-context-reference.md)
