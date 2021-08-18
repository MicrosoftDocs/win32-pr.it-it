---
title: Visualizzazione di interfacce utente modali
description: Visualizzazione di interfacce utente modali
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player plug-in, visualizzazione di finestre di dialogo e di messaggi
- plug-in, visualizzazione di finestre di dialogo e di messaggi
- plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e di messaggi
- plug-in dell'interfaccia utente, visualizzazione di finestre di dialogo e di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addacfe2a309808f949c59a8ec11498417cb05a17cd6ab160ca1c08d2017a0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997241"
---
# <a name="displaying-modal-user-interfaces"></a>Visualizzazione di interfacce utente modali

I plug-in dell'interfaccia utente non devono visualizzare finestre di dialogo modali o finestre di messaggio in risposta alle chiamate ai metodi Windows Media Player. Ad esempio, non visualizzare una finestra di messaggio dall'implementazione di **IWMPPluginUI::Create**.

Se è necessario visualizzare una finestra di dialogo o una finestra di messaggio dall'implementazione di un metodo del plug-in dell'interfaccia utente chiamato dal lettore, è necessario seguire questa procedura:

1.  Registrare un nuovo messaggio di finestra **usando RegisterWindowMessage.**
2.  Inviare il messaggio della finestra registrato alla finestra del plug-in dell'interfaccia utente usando **PostMessage.**
3.  Visualizzare la finestra di dialogo o la finestra di messaggio dal gestore di messaggi per il nuovo messaggio della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica del plug-in dell'interfaccia utente**](ui-plug-in-overview.md)
</dt> </dl>

 

 




