---
description: Un dispositivo telefonico può avere più dispositivi hookswitch.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivi hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527601"
---
# <a name="hookswitch-devices"></a>Dispositivi hookswitch

Un dispositivo telefonico può avere più dispositivi hookswitch. Un hookswitch è l'opzione che connette o disconnette un dispositivo dalla linea telefonica. In un telefono, ad esempio, si tratta dell'opzione che viene attivata automaticamente quando un utente solleva il ricevitore dalla culla per ottenere un nuovo tono di composizione. TAPI definisce tre tipi di dispositivi hookswitch per un telefono: portatile, vivavoce e auricolare. Ogni dispositivo hookswitch dispone di un altoparlante e di un componente Microphone e funziona in una delle quattro modalità hookswitch:

-   **OnHook** Il dispositivo hookswitch è OnHook e il microfono e l'altoparlante sono disabilitati.
-   **Solo microfono** Il dispositivo hookswitch è Offhook, il microfono è abilitato e il relativo altoparlante è disattivato.
-   **Solo altoparlante** Il dispositivo hookswitch è Offhook, il microfono è disattivato e il relativo altoparlante è abilitato.
-   **Microfono e altoparlante** Il dispositivo hookswitch è Offhook ed entrambi i microfoni e gli speaker sono abilitati.

La funzione [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) viene usata per impostare la modalità hookswitch di uno o più dispositivi hookswitch di un dispositivo telefonico aperto. Ad esempio, per disattivare o disattivare il microfono o il componente altoparlante di un dispositivo hookswitch, usare **phoneSetHookSwitch** con la modalità hookswitch appropriata. La funzione [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) può essere usata per eseguire una query sulla modalità hookswitch di un dispositivo hookswitch di un dispositivo telefonico aperto.

Quando la modalità del dispositivo hookswitch del telefono viene modificata manualmente, ad esempio sollevando il ricevitore dalla propria culla, viene inviato un messaggio di [**\_ stato del telefono**](phone-state.md) all'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

Il volume del componente Speaker di un dispositivo hookswitch può essere impostato con [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). L'impostazione del volume è diversa da quella di silenziamento, in quanto la tacitazione di un altoparlante e la successiva disabilitazione consentiranno di mantenere l'impostazione del volume dell'altoparlante. La funzione [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) può essere usata per restituire l'impostazione del volume corrente dell'altoparlante di un dispositivo hookswitch di un dispositivo telefonico aperto.

Anche il componente Microphone di un dispositivo hookswitch può essere controllato. L'impostazione del guadagno è diversa da quella di silenziamento in quanto la tacitazione di un microfono e la successiva riattivazione consentirà di mantenere l'impostazione di guadagno del microfono. Usare [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) per impostare il guadagno del microfono di un dispositivo hookswitch di un dispositivo telefonico aperto e [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) per restituire l'impostazione di guadagno del microfono di un dispositivo hookswitch di un telefono aperto.

Quando viene modificato il volume o il guadagno del dispositivo hookswitch del telefono, \_ viene inviato un messaggio di stato telefonico alla funzione dell'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



