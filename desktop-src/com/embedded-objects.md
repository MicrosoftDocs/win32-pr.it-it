---
title: Oggetti incorporati (COM)
description: Oggetti incorporati
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118798"
---
# <a name="embedded-objects-com"></a>Oggetti incorporati (COM)

Un oggetto incorporato viene memorizzato fisicamente nel documento composto insieme a tutte le informazioni necessarie per la gestione dell'oggetto. In altre parole, l'oggetto incorporato è effettivamente una parte del documento composto in cui risiede. Questa disposizione presenta alcuni svantaggi. In primo luogo, un documento composto contenente oggetti incorporati sarà maggiore di uno contenente gli stessi oggetti dei collegamenti. In secondo luogo, le modifiche apportate all'origine di un oggetto incorporato non verranno replicate automaticamente nella copia incorporata e le modifiche apportate alla copia incorporata non verranno riflesse nell'origine, come avviene con un collegamento.

Tuttavia, per determinati scopi, l'incorporamento offre diversi vantaggi rispetto ai collegamenti. In primo luogo, gli utenti possono trasferire i documenti composti con oggetti incorporati ad altri computer o altri percorsi nello stesso computer senza suddividere un collegamento. In secondo luogo, gli utenti possono modificare gli oggetti incorporati senza modificare il contenuto dell'originale. In alcuni casi, questa separazione è esattamente ciò che è necessario. Terzo, gli oggetti incorporati possono essere attivati sul posto, ovvero l'utente può modificare o manipolare l'oggetto senza dover lavorare in una finestra separata da quella del contenitore dell'oggetto. Al contrario, quando l'oggetto viene attivato, l'interfaccia utente dell'applicazione contenitore cambia per esporre gli strumenti necessari per la gestione o la modifica dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di oggetti collegati e incorporati da dati esistenti](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




