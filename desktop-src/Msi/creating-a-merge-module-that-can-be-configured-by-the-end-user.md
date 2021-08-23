---
description: Per creare moduli unione, usare le linee guida generali descritte nell'argomento Creazione di moduli unione.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Creazione di un modulo unione che può essere configurato dal End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d1b4ffebe21659d33640c3872e9e6c7875518654b86d256ea4b858444ef39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948135"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Creazione di un modulo unione che può essere configurato dal End-User

Per creare moduli unione, usare le linee guida generali descritte [nell'argomento Creazione di moduli unione.](authoring-merge-modules.md) È inoltre necessario eseguire le operazioni seguenti per creare un modulo unione che può essere configurato dall'utente finale del modulo:

-   Gli utenti finali devono avere Mergemod.dll versione 2.0 per configurare il modulo. Gli utenti che dispongono di versioni precedenti Mergemod.dll possono applicare il modulo, ma ottengono sempre le impostazioni predefinite.
-   Aggiungere una [tabella ModuleConfiguration](moduleconfiguration-table.md) al modulo unione per identificare gli elementi che possono essere configurati da un utente finale. Aggiungere un record in questa tabella per ogni elemento configurabile. Questi elementi vengono sostituiti nei modelli specificati nella [tabella ModuleSubstitution .](modulesubstitution-table.md) Immettere un nome per ogni elemento configurabile nel campo Nome. Immettere il formato, il tipo e il contesto semantico per ogni elemento nelle colonne Format, Type e ContextData. Per altre informazioni, vedere [Tipi semantici](semantic-types.md). Immettere un valore predefinito per l'elemento nel campo DefaultValue usando [il formato speciale CMSM](cmsm-special-format.md).
-   Aggiungere una [tabella ModuleSubstitution](modulesubstitution-table.md) al modulo unione. Ogni record in questa tabella corrisponde a una sostituzione di uno o più elementi configurabili in un campo del database del modulo unione. Immettere la tabella, la riga e la colonna del campo che riceve la sostituzione. Immettere un modello di formattazione per la sostituzione nella colonna Valore usando [il formato speciale CMSM](cmsm-special-format.md).
-   Aggiungere record alla tabella [di convalida](-validation-table.md) per le tabelle ModuleSubstitution e ModuleConfiguration.
-   Aggiungere record alla [tabella ModuleIgnoreTable](moduleignoretable-table.md) per [la tabella ModuleSubstitution e](modulesubstitution-table.md) alla tabella [ModuleConfiguration](moduleconfiguration-table.md). Ciò garantisce che il modulo sia compatibile per gli utenti che dispongono di versioni di Mergemod.dll precedenti alla versione 2.0.

 

 



