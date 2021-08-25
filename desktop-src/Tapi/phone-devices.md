---
description: Telefono il supporto dei dispositivi è supplementare anziché di base, quindi i provider di servizi non sono tenuti a supportare i dispositivi telefonici.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Telefono Dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d11aa269e17d74fbaf74c701c954ced734ef33900198a7c9e30a044f5ebd32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873281"
---
# <a name="phone-devices"></a>Telefono Dispositivi

Telefono il supporto dei dispositivi è supplementare anziché di base, quindi i provider di servizi non sono tenuti a supportare i dispositivi telefonici.

Proprio come una classe di dispositivi line è un'astrazione di un dispositivo linea fisico, la classe del dispositivo telefonico rappresenta un'astrazione indipendente dal dispositivo di un set di telefoni. TAPI considera i dispositivi line e phone come dispositivi indipendenti l'uno dall'altro. In altre parole, è possibile usare un telefono (dispositivo) senza usare una linea associata ed è possibile usare una linea (dispositivo) senza usare un telefono.

I provider di servizi che implementano completamente questa indipendenza possono offrire usi per questi dispositivi non definiti dai protocolli di telefonia tradizionali. Ad esempio, una persona può usare il telefono del desktop come dispositivo audio waveform per la registrazione vocale o la riproduzione, probabilmente senza che l'interruttore sia a conoscenza del fatto che il telefono è in uso. In un'implementazione di questo tipo, il lifting del telefono locale non deve inviare automaticamente un segnale offhook al commutatore.

Questa indipendenza consente inoltre a un'applicazione di usare il telefono locale in modo indipendente dalle chiamate in ingresso. Le funzionalità dei provider di servizi sono limitate dalle funzionalità dell'hardware e del software usate per interconnettere il commutatore, il telefono e il computer.

TAPI include funzioni per recuperare le funzionalità del dispositivo che consentono ai client di determinare se tale modello di utilizzo è supportato.

Questa sezione descrive i dispositivi telefonici e spiega come usare le funzioni del telefono TAPI per accedere a questi dispositivi.

-   [Telefono Dispositivo](phone-device-elements.md)
-   [Inizializzazione e arresto](initialization-and-shutdown.md)

 

 



