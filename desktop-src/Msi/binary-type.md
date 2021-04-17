---
description: Il tipo binario del tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave nella tabella binaria fornita dall'utente.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo binario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528860"
---
# <a name="binary-type"></a>Tipo binario

Il tipo binario del [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave nella [tabella binaria](binary-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo. Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per garantire che l'utente fornisca una chiave valida nella tabella binaria.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo binario può essere utilizzato con i tipi di ContextData seguenti.

**Bitmap ContextData**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine bitmap. Mergmod.dll non garantisce dimensioni o tipi di bitmap specifici e lo strumento di merge deve garantire che i dati siano un'immagine valida. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "binary" nella colonna tipo e immettere "bitmap" nella colonna ContextData della tabella ModuleConfiguration.

**Icona ContextData**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine di icona. Mergmod.dll non garantisce alcuna dimensione o tipo di icona specifica e lo strumento di merge deve garantire che i dati siano un'immagine valida. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "binary" nella colonna tipo e immettere "Icon" nella colonna ContextData della tabella ModuleConfiguration. Questo tipo non è appropriato per l'utilizzo in una tabella degli annunci.

**ContextData EXE**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine eseguibile a 32 bit. Mergmod.dll non convalida i dati sono validi e lo strumento di merge deve garantire che i dati siano un file PE valido. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "binary" nella colonna tipo e immettere "EXE" nella colonna ContextData della tabella ModuleConfiguration.

**ContextData EXE64**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine eseguibile a 32 bit o a 64 bit. Mergmod.dll non convalida i dati sono validi e lo strumento di merge deve garantire che i dati siano un file PE valido. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "binary" nella colonna tipo e immettere "EXE64" nella colonna ContextData della tabella ModuleConfiguration.

 

 



