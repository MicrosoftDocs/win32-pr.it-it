---
title: Informazioni sullo schema di Active Directory
description: Ogni oggetto in Active Directory Domain Services è un'istanza di una classe di oggetti definita nello schema di Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855206"
---
# <a name="about-the-active-directory-schema"></a>Informazioni sullo schema di Active Directory

Ogni oggetto in Active Directory Domain Services è un'istanza di una classe di oggetti definita nello schema di Active Directory. Una classe di oggetti rappresenta una categoria di oggetti, quali utenti, stampanti o applicazioni, che condividono un insieme di caratteristiche comuni. La definizione di ciascuna classe di oggetti contiene l'elenco degli attributi che possono essere utilizzati per descrivere le istanze della classe. Ad esempio, la classe User dispone di attributi quali **givenName**, **surname** e **streetAddress**. L'elenco di attributi per una classe è diviso in quelli che un oggetto di tale classe deve contenere e attributi aggiuntivi che possono essere contenuti in un oggetto. La directory viene disposta in una gerarchia. la definizione di ogni classe elenca anche le classi i cui oggetti possono essere elementi padre di oggetti di una determinata classe, che controlla la forma della gerarchia di directory.

Lo schema definisce formalmente anche ogni attributo. La definizione per ogni attributo include identificatori univoci per l'attributo, la sintassi per l'attributo (ovvero il tipo di dati per i valori dell'attributo), i limiti di intervallo facoltativi per i valori di attributo, se l'attributo può avere un solo valore o più valori e se l'attributo è indicizzato. Lo schema di directory definisce ogni attributo una sola volta, ovvero le definizioni delle classi di oggetti contengono riferimenti agli attributi definiti nello schema. Ad esempio, l'attributo "Description" viene definito una sola volta e vi viene fatto riferimento da molte classi di oggetti. Questa operazione è diversa rispetto a uno schema di database relazionale, in cui gli "attributi" (colonne) sono definiti separatamente per ogni tabella.

 

 




