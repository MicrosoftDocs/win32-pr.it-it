---
title: Componente provider di esempio ADSI
description: Active Directory i writer del provider di interfacce del servizio troveranno questa sezione di particolare interesse, perché descrive in modo dettagliato il componente del provider di esempio ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328452"
---
# <a name="adsi-example-provider-component"></a>Componente provider di esempio ADSI

Active Directory i writer del provider di interfacce del servizio troveranno questa sezione di particolare interesse, perché descrive in modo dettagliato il componente del provider di esempio ADSI. I writer del provider ADSI possono installare il provider di esempio e utilizzare il Framework di codice come base per creare la propria implementazione. Vengono trattati i seguenti argomenti:

L' [installazione del componente provider di esempio](installing-the-example-provider-component.md) descrive come installare il provider di esempio ADSI e la relativa directory fittizia. Questa sezione include un elenco delle impostazioni del registro di sistema.

La [definizione della directory](directory-definition.md) descrive le voci di directory definite dal componente provider di esempio.

[Gestione schema](schema-management.md) descrive il modo in cui ogni elemento nel servizio directory del componente provider di esempio può essere rappresentato da un tipo specifico di oggetto Active Directory.

Il [binding a un oggetto Active Directory](binding-to-an-active-directory-object.md) descrive in che modo, data una stringa ADsPath, il componente provider di esempio identifica tale elemento, crea il tipo appropriato di Active Directory oggetto e recupera il tipo di puntatore di interfaccia richiesto su tale oggetto per passare di nuovo al software client ADS.

[Oggetti enumeratore](enumerator-objects.md) elenca i tipi specifici di enumerazioni fornite dal componente provider di esempio e il codice sorgente in cui è possibile trovare le implementazioni.

[Cenni preliminari sul codice](code-overview.md) fornisce una descrizione a livello di attività di ogni parte del componente provider di esempio.

[Dettagli codice](code-details.md) elenca i moduli software e il relativo contenuto.

 

 




