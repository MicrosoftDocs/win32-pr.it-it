---
description: Per creare i moduli unione, utilizzare le linee guida generali descritte nell'argomento authoring merge modules.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Creazione di un modulo merge che può essere configurato dalla End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232263"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Creazione di un modulo merge che può essere configurato dalla End-User

Per creare i moduli unione, utilizzare le linee guida generali descritte nell'argomento [Authoring merge modules](authoring-merge-modules.md) . Per creare un modulo merge che può essere configurato dall'utente finale del modulo, è inoltre necessario eseguire le operazioni seguenti:

-   Gli utenti finali devono avere Mergemod.dll versione 2,0 per configurare il modulo. Gli utenti che hanno versioni precedenti di Mergemod.dll possono applicare il modulo, ma ottengono sempre le impostazioni predefinite.
-   Aggiungere una [tabella ModuleConfiguration](moduleconfiguration-table.md) al modulo merge per identificare gli elementi che possono essere configurati da un utente finale. Aggiungere un record in questa tabella per ogni elemento configurabile. Questi elementi sono sostituiti dai modelli specificati nella [tabella ModuleSubstitution](modulesubstitution-table.md). Immettere un nome per ogni elemento configurabile nel campo nome. Immettere il formato, il tipo e il contesto semantico per ogni elemento nelle colonne format, Type e ContextData. Per altre informazioni, vedere [tipi semantici](semantic-types.md). Immettere un valore predefinito per l'elemento nel campo DefaultValue usando il [formato speciale CMSM](cmsm-special-format.md).
-   Aggiungere una [tabella ModuleSubstitution](modulesubstitution-table.md) al modulo merge. Ogni record di questa tabella corrisponde a una sostituzione di uno o più elementi configurabili in un campo del database del modulo merge. Immettere la tabella, la riga e la colonna del campo che riceve la sostituzione. Immettere un modello di formattazione per la sostituzione nella colonna valore utilizzando il [formato speciale CMSM](cmsm-special-format.md).
-   Aggiungere record alla [tabella di convalida](-validation-table.md) per le tabelle ModuleSubstitution e ModuleConfiguration.
-   Aggiungere i record alla tabella [ModuleIgnoreTable](moduleignoretable-table.md) per la tabella [ModuleSubstitution](modulesubstitution-table.md) e la [tabella ModuleConfiguration](moduleconfiguration-table.md). Ciò garantisce che il modulo sia compatibile per gli utenti che hanno versioni di Mergemod.dll precedenti alla versione 2,0.

 

 



