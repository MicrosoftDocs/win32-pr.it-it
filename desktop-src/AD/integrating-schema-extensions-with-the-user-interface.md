---
title: Integrazione di estensioni dello schema con l'interfaccia utente
description: Gli strumenti di amministrazione di Active Directory Domain Services utilizzano un'architettura comune per connettere l'interfaccia utente amministrativa allo schema di directory.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297727"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Integrazione di estensioni dello schema con l'interfaccia utente

Gli strumenti di amministrazione di Active Directory Domain Services utilizzano un'architettura comune per connettere l'interfaccia utente amministrativa allo schema di directory. Il fulcro di questa architettura è la classe di oggetti **displaySpecifier** . Gli identificatori di visualizzazione e il relativo utilizzo sono descritti in dettaglio in [estensione dell'interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md).

Quando si crea una nuova classe creando una sottoclasse di una classe esistente, è possibile utilizzare l'interfaccia utente esistente per la superclasse copiando l'identificatore di visualizzazione della superclasse. Un modo semplice per copiare l'identificatore di visualizzazione per una classe consiste nell'esportarlo in un file LDIF utilizzando LDIFDE, modificare il nome distinto e il CN, quindi importare il file LDIF modificato. Se la sottoclasse ha attributi aggiuntivi, sarà necessario fornire altre pagine delle proprietà per supportare la modifica. Se la sottoclasse dispone di proprietà aggiuntive, è necessario fornire le pagine di estensione della finestra di dialogo di creazione perché l'interfaccia utente fornita dalla superclasse non ha modo di creare questi nuovi attributi.

 

 




