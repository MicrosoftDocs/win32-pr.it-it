---
description: Il supporto dei dispositivi telefonici è supplementare anziché Basic, quindi i provider di servizi non devono supportare i dispositivi telefonici.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivi telefonici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966854"
---
# <a name="phone-devices"></a>Dispositivi telefonici

Il supporto dei dispositivi telefonici è supplementare anziché Basic, quindi i provider di servizi non devono supportare i dispositivi telefonici.

Proprio come una classe di dispositivo linea è un'astrazione di un dispositivo a linee fisico, la classe del dispositivo Phone rappresenta un'astrazione indipendente dal dispositivo di un set di telefono. TAPI considera i dispositivi line e Phone come dispositivi indipendenti l'uno dall'altro. In altre parole, è possibile usare un telefono (dispositivo) senza usare una riga associata ed è possibile usare una linea (dispositivo) senza usare un telefono.

I provider di servizi che implementano completamente questa indipendenza possono offrire usi per questi dispositivi non definiti dai protocolli di telefonia tradizionali. Ad esempio, una persona può usare il telefono del telefono del desktop come dispositivo audio della forma d'onda per la registrazione o la riproduzione vocale, probabilmente senza la conoscenza del comunicatore che il telefono è in uso. In tale implementazione, il sollevamento del dispositivo telefonico locale non deve inviare automaticamente un segnale Offhook al Commuter.

Questa indipendenza consente anche a un'applicazione di squillare il telefono locale in modo indipendente dalle chiamate in ingresso. Le funzionalità dei provider di servizi sono limitate dalle funzionalità dell'hardware e del software utilizzati per collegare il commutirio, il telefono e il computer.

TAPI include funzioni per recuperare le funzionalità del dispositivo che consentono ai client di determinare se tale modello di utilizzo è supportato.

In questa sezione vengono descritti i dispositivi telefonici e viene illustrato come utilizzare le funzioni del telefono TAPI per accedere a tali dispositivi.

-   [Dispositivo telefonico](phone-device-elements.md)
-   [Inizializzazione e arresto](initialization-and-shutdown.md)

 

 



