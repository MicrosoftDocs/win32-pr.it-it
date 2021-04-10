---
description: Il tipo enum del tipo semantico è uno dei tipi di formato testo.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967145"
---
# <a name="enum-type"></a>Tipo enum

Il tipo enum del [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo scelta dall'utente da un set di opzioni. Lo strumento di merge sostituisce la stringa selezionata selezionata nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "enum" nella colonna tipo e immettere l'elenco di stringhe possibili nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). L'elenco di stringhe possibili deve essere fornito come un elenco di stringhe deliminated da punti e virgola. Ogni scelta deve avere il formato "nome = valore". È possibile aggiungere un punto e virgola letterale al valore anteponendo il punto e virgola con un carattere barra rovesciata. Null è un valore valido a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.

 

 



