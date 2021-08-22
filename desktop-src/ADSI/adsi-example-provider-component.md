---
title: Componente provider di esempio ADSI
description: I writer di provider di Active Directory Service Interfaces troveranno questa sezione di particolare interesse, perché descrive in modo approfondito il componente provider di esempio ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ff1d998a9db620c6dc6fb4402f126f556c95a45d589410800ea9c4b335a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023899"
---
# <a name="adsi-example-provider-component"></a>Componente provider di esempio ADSI

I writer di provider di Active Directory Service Interfaces troveranno questa sezione di particolare interesse, perché descrive in modo approfondito il componente provider di esempio ADSI. I writer del provider ADSI possono installare il provider di esempio e usare il framework di codice come base per creare la propria implementazione. Vengono trattati i seguenti argomenti:

[Installazione del componente provider di esempio](installing-the-example-provider-component.md) descrive come installare il provider di esempio ADSI e la relativa directory fittizia. Questa sezione include un elenco delle impostazioni del Registro di sistema.

[Definizione directory](directory-definition.md) descrive le voci di directory definite dal componente provider di esempio.

[Gestione schemi](schema-management.md) descrive come ogni elemento nel servizio directory dei componenti del provider di esempio può essere rappresentato da un tipo specifico di oggetto Active Directory.

[L'associazione](binding-to-an-active-directory-object.md) a un oggetto Active Directory descrive come, data una stringa ADsPath, il componente provider di esempio identifichi tale elemento, crei il tipo appropriato di oggetto Active Directory e recuperi il tipo richiesto di puntatore a interfaccia su tale oggetto da passare nuovamente al software client ADs.

[Enumerator Objects](enumerator-objects.md) elenca i tipi specifici di enumerazioni forniti dal componente provider di esempio e in cui è possibile trovare il codice sorgente delle implementazioni.

[Panoramica del codice](code-overview.md) fornisce una descrizione a livello di attività di ogni parte del componente provider di esempio.

[Dettagli codice elenca](code-details.md) i moduli software e il relativo contenuto.

 

 




