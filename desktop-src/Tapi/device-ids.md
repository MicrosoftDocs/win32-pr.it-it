---
description: Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefonico aperto per identificare il dispositivo telefono aperto.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: ID dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307204"
---
# <a name="device-ids"></a>ID dei dispositivi

Altre funzioni telefoniche TAPI usano un handle per un dispositivo telefonico aperto per identificare il dispositivo telefono aperto. Le uniche funzioni per i dispositivi telefonici che accettano un parametro dell'identificatore del dispositivo telefonico (in contrapposizione a un handle telefonico) sono le funzioni [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) . Un'applicazione può recuperare l'identificatore del dispositivo del telefono usando la funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) con l'handle telefonico come parametro.

Un'applicazione può anche ottenere gli identificatori di dispositivo per varie classi di dispositivi associate a un telefono aperto richiamando [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Vedere [le classi di dispositivi TAPI](tapi-device-classes.md) per i nomi delle classi di dispositivi.

Questa funzione accetta un handle del telefono e una descrizione della classe del dispositivo. Restituisce l'identificatore del dispositivo per il dispositivo della classe del dispositivo specificata associata al dispositivo telefonico aperto. Se la classe del dispositivo è "TAPI/Phone", viene restituito l'identificatore del dispositivo del telefono.

A differenza dei dispositivi line, per i quali i servizi linea di base forniscono l'equivalente di POTS, non viene definito alcun set di funzioni minimo garantito per i dispositivi telefonici. Sebbene ogni dispositivo telefonico fornisca almeno le funzioni e i messaggi descritti in questa sezione, non offre alcuna operazione effettiva sul dispositivo telefonico fisico.

 

 



