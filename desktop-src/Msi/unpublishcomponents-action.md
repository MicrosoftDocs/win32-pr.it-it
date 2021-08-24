---
description: L'azione UnpublishComponents gestisce l'annullamento della modifica dei componenti elencati nella tabella PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Azione UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810261"
---
# <a name="unpublishcomponents-action"></a>Azione UnpublishComponents

L'azione UnpublishComponents gestisce l'annullamento della modifica dei componenti elencati nella tabella PublishComponent. Si tratta di componenti che potrebbero essere in errore da altri prodotti. Questa azione rimuove le informazioni sui componenti pubblicati dalla tabella [PublishComponent](publishcomponent-table.md) per cui la funzionalità corrispondente è attualmente selezionata per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID che rappresenta l'ID componente di una funzionalità annunciata. |
| \[2\] | Qualificatore dell'ID componente.                               |



 

