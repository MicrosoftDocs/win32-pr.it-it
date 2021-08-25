---
description: Il tipo Enum di tipo semantico è uno dei tipi di formato testo.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869321"
---
# <a name="enum-type"></a>Tipo enum

Il tipo Enum di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo scelta dall'utente da un set di scelte. Lo strumento di unione sostituisce la stringa selezionata nei modelli specificati nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna Nome, immettere "0" nella colonna Formato, immettere "Enum" nella colonna Tipo e immettere l'elenco di stringhe possibili nella colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md). L'elenco di possibili stringhe deve essere fornito come elenco di stringhe deliminate da punti e virgola. Ogni scelta deve essere nel formato "Nome=Valore". È possibile aggiungere un punto e virgola letterale al valore anteficcando il punto e virgola con un carattere barra rovesciata. Null è un valore valido a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della tabella ModuleConfiguration.

 

 



