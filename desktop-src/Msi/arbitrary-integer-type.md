---
description: Il tipo Integer arbitrario di tipo semantico è uno dei tipi di formato integer.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo Integer arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131494"
---
# <a name="arbitrary-integer-type"></a>Tipo Integer arbitrario

Il tipo Integer arbitrario di [tipo semantico](semantic-types.md) è uno dei [tipi di formato integer](integer-format-types.md). Questo tipo di elemento configurabile è un integer fornito dall'utente. Lo strumento di merge sostituisce questo Integer nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "2" nella colonna formato e lasciare vuote le colonne Type e ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). Le colonne Type e ContextData sono riservate e devono essere null.

 

 



