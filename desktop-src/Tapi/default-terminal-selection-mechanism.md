---
description: Il concetto del terminale multitracking rende ancora più utile per TAPI fornire un metodo semplificato per la selezione di un terminale in un flusso o in flussi. Il meccanismo predefinito di selezione dei terminali è progettato per risolvere questo problema.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Meccanismo di selezione terminali predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878898"
---
# <a name="default-terminal-selection-mechanism"></a>Meccanismo di selezione terminali predefinito

Il concetto del [terminale multitracking](multitrack-terminals.md) rende ancora più utile per TAPI fornire un metodo semplificato per la selezione di un terminale in un flusso o in flussi. Il meccanismo predefinito di selezione dei terminali è progettato per risolvere questo problema.

## <a name="selecting-a-terminal-on-a-call"></a>Selezione di un terminale in una chiamata

La funzionalità di selezione dei terminali predefinita viene fornita tramite la possibilità di selezionare un terminale in una chiamata.

L' [oggetto call](call-object.md) espone una nuova interfaccia, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). L'interfaccia espone gli stessi metodi di [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), più tre nuovi metodi: [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)e [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).

**ITBasicCallControl2:: RequestTerminal** crea un terminale, dati la classe terminale, la direzione e il tipo di supporto. Esamina gli elenchi dei terminali statici e dinamici supportati per trovare e creare il terminale richiesto.

[**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) seleziona il terminale (o, nel caso di un terminale multitraccia, enumera, crea se necessario e seleziona i terminali Track) sul flusso (o sui flussi) disponibili per la chiamata.

L'algoritmo per la corrispondenza dei flussi di chiamata al terminale o alle tracce disponibili nel terminale è descritto nella documentazione di [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

La chiamata a [**ITBasicCallControl2:: UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) fa sì che il terminale (Single-Track o Multitrack) venga deselezionato dalla chiamata. Per ulteriori informazioni, vedere la documentazione del metodo.

## <a name="selecting-a-terminal-on-itstream"></a>Selezione di un terminale in ITStream

Se si seleziona un terminale a traccia singola in [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (chiamando [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)), viene selezionato il terminale nel flusso. Si tratta della normale procedura di selezione dei terminali TAPI 3.

In un flusso è possibile selezionare solo terminali con tracce singole. La selezione di un terminale multitraccia in un flusso avrà esito negativo, poiché il flusso non riconoscerà il tipo e la direzione del supporto.

 

 
