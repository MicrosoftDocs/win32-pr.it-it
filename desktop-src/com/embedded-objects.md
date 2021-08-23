---
title: Oggetti incorporati (COM)
description: Oggetti incorporati
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df671850dc167a0751f69cbc57f8c19698db06a0454dd6283553c4d8ffa1609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048359"
---
# <a name="embedded-objects-com"></a>Oggetti incorporati (COM)

Un oggetto incorporato viene archiviato fisicamente nel documento composto, insieme a tutte le informazioni necessarie per gestire l'oggetto. In altre parole, l'oggetto incorporato è in realtà una parte del documento composto in cui risiede. Questa disposizione presenta un paio di svantaggi. In primo luogo, un documento composto contenente oggetti incorporati sarà più grande di uno contenente gli stessi oggetti dei collegamenti. In secondo piano, le modifiche apportate all'origine di un oggetto incorporato non verranno replicate automaticamente nella copia incorporata e le modifiche nella copia incorporata non verranno riflesse nell'origine, come si fa con un collegamento.

Tuttavia, per determinati scopi, l'incorporamento offre diversi vantaggi rispetto ai collegamenti. In primo luogo, gli utenti possono trasferire documenti composti con oggetti incorporati in altri computer o in altre posizioni nello stesso computer, senza interrompere un collegamento. In secondo piano, gli utenti possono modificare gli oggetti incorporati senza modificare il contenuto dell'originale. A volte, questa separazione è esattamente ciò che è necessario. In terzo luogo, gli oggetti incorporati possono essere attivati sul posto, vale a dire che l'utente può modificare o modificare in altro modo l'oggetto senza dover lavorare in una finestra separata da quella del contenitore dell'oggetto. Al contrario, quando l'oggetto viene attivato, l'interfaccia utente dell'applicazione contenitore cambia per esporre gli strumenti necessari per gestire o modificare l'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di oggetti collegati e incorporati da dati esistenti](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




