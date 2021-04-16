---
description: L'azione UnpublishComponents gestisce l'unadvertising dei componenti elencati nella tabella PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Azione UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104401918"
---
# <a name="unpublishcomponents-action"></a>Azione UnpublishComponents

L'azione UnpublishComponents gestisce l'unadvertising dei componenti elencati nella tabella PublishComponent. Si tratta di componenti che possono avere errori in altri prodotti. Questa azione consente di rimuovere informazioni sui componenti pubblicati dalla [tabella PublishComponent](publishcomponent-table.md) per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID che rappresenta l'ID componente di una funzionalità annunciata. |
| \[2\] | Qualificatore dell'ID componente.                               |



 

