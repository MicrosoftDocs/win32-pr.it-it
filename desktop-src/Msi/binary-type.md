---
description: Il tipo binario di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave nella tabella binaria fornita dall'utente.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo binario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8412d63891f3028c1ef2beb8fa0e6a17c4a35c33df182cbd9f1059a593c50915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105371"
---
# <a name="binary-type"></a>Tipo binario

Il tipo binario [di tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave nella [tabella binaria](binary-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un identificatore Windows installer [valido](identifier.md) per gli elementi di questo tipo. Mergemod.dll non applica questa restrizione ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella binaria.

Null è un valore valido per questo tipo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo Binary può essere usato con i tipi di ContextData seguenti.

**Bitmap ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna a una riga della tabella binaria che contiene un'immagine bitmap. Mergmod.dll non garantisce dimensioni o tipi specifici di bitmap e lo strumento di unione deve garantire che i dati siano un'immagine valida. Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Binary" nella colonna Tipo e immettere "Bitmap" nella colonna ContextData della tabella ModuleConfiguration.

**Icona ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine di icona. Mergmod.dll non garantisce dimensioni o tipi specifici di icona e lo strumento di unione deve garantire che i dati siano un'immagine valida. Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Binary" nella colonna Tipo e immettere "Icon" nella colonna ContextData della tabella ModuleConfiguration. Questo tipo non è appropriato per l'uso in una tabella di annunci.

**EXE ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna a una riga della tabella binaria che contiene un'immagine eseguibile a 32 bit. Mergmod.dll non convalida la validità dei dati e lo strumento di unione deve garantire che i dati siano un file PE valido. Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Binary" nella colonna Tipo e immettere "EXE" nella colonna ContextData della tabella ModuleConfiguration.

**EXE64 ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella binaria che contiene un'immagine eseguibile a 32 bit o a 64 bit. Mergmod.dll non convalida la validità dei dati e lo strumento di unione deve garantire che i dati siano un file PE valido. Per specificare un elemento configurabile di questo tipo, gli autori del modulo devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Binary" nella colonna Tipo e immettere "EXE64" nella colonna ContextData della tabella ModuleConfiguration.

 

 



