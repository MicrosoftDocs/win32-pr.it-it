---
title: Integrazione delle estensioni dello schema con il Interfaccia utente
description: Gli strumenti di amministrazione di Active Directory Domain Services un'architettura comune per la connessione dell'interfaccia utente amministrativa allo schema di directory.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187210"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrazione delle estensioni dello schema con il Interfaccia utente

Gli strumenti di amministrazione di Active Directory Domain Services un'architettura comune per la connessione dell'interfaccia utente amministrativa allo schema di directory. La parte centrale di questa architettura è la **classe dell'oggetto displaySpecifier.** Gli identificatori di visualizzazione e il relativo utilizzo sono descritti in dettaglio in [Extending the Interfaccia utente for Directory Objects](extending-the-user-interface-for-directory-objects.md).

Quando si crea una nuova classe sottoclassando una classe esistente, è possibile sfruttare l'interfaccia utente esistente per la superclasse copiando l'identificatore di visualizzazione della superclasse. Un modo semplice per copiare l'identificatore di visualizzazione per una classe è esportarlo in un file LDIF usando LDIFDE, modificare il nome distinto e cn, quindi importare il file LDIF modificato. Se la sottoclasse ha attributi aggiuntivi, sarà necessario fornire pagine delle proprietà aggiuntive per supportare la modifica. Se la sottoclasse ha proprietà obbligatorie aggiuntive, sarà necessario fornire pagine di estensione della finestra di dialogo di creazione perché l'interfaccia utente fornita dalla superclasse non è in grado di creare questi nuovi attributi.

 

 




