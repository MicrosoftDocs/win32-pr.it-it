---
description: Un dispositivo telefono può avere più dispositivi hookswitch.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivi Hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca5c9f605731780068b9ad5a5b35d913213006c62d127e6a3b15d1ffc5fe1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013101"
---
# <a name="hookswitch-devices"></a>Dispositivi Hookswitch

Un dispositivo telefono può avere più dispositivi hookswitch. Un hookswitch è l'interruttore che connette o disconnette un dispositivo dalla linea telefonica. In un telefono, ad esempio, si tratta dell'interruttore che viene attivato automaticamente quando un utente solleva il ricevitore dalla culla per ottenere un nuovo segnale acustico. TAPI definisce tre tipi di dispositivi hookswitch per un telefono: ricevitore, altoparlante e visore. Ogni dispositivo hookswitch ha un altoparlante e un componente microfono e opera in una delle quattro modalità hookswitch:

-   **Onhook** Il dispositivo hookswitch è onhook e sia il microfono che l'altoparlante sono disabilitati.
-   **Solo microfono** Il dispositivo hookswitch è offhook, il microfono è abilitato e l'altoparlante è disattivato.
-   **Solo voce** Il dispositivo hookswitch è offhook, il microfono è disattivato e il relativo altoparlante è abilitato.
-   **Microfono e altoparlante** Il dispositivo hookswitch è offhook e sono abilitati sia il microfono che l'altoparlante.

La [**funzione phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) viene usata per impostare la modalità hookswitch di uno o più dispositivi hookswitch di un dispositivo telefono aperto. Ad esempio, per disattivare o riattivare il microfono o il componente altoparlante di un dispositivo hookswitch, usare **phoneSetHookSwitch** con la modalità hookswitch appropriata. La [**funzione phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) può essere usata per eseguire query sulla modalità hookswitch di un dispositivo hookswitch di un dispositivo telefono aperto.

Quando la modalità del dispositivo hookswitch di un telefono viene modificata manualmente, ad esempio sollevando il ricevitore dalla culla, viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) all'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

Il volume del componente speaker di un dispositivo hookswitch può essere impostato [**con phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). L'impostazione del volume è diversa dall'disattivazione dell'audio in quanto la disattivazione dell'audio di un altoparlante e la successiva riattivazione dell'audio mantengono l'impostazione del volume dell'altoparlante. La [**funzione phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) può essere usata per restituire l'impostazione corrente del volume dell'altoparlante di un dispositivo hookswitch di un dispositivo telefono aperto.

Anche il componente microfono di un dispositivo hookswitch può essere controllato. L'impostazione Gain è diversa dall'audio in quanto la disattivazione di un microfono e la successiva riattivazione del microfono mantengono l'impostazione di guadagno del microfono. Usare [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) per impostare il guadagno del microfono di un dispositivo hookswitch di un dispositivo telefono aperto e [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) per restituire l'impostazione di guadagno del microfono di un dispositivo hookswitch di un telefono aperto.

Quando il volume o il guadagno del dispositivo hookswitch di un telefono viene modificato, viene inviato un messaggio PHONE STATE alla funzione dell'applicazione per notificare all'applicazione la modifica \_ dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



