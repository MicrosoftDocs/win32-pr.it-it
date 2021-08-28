---
description: È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000.msp creata in Generazione di un pacchetto patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Applicazione di un pacchetto patch a un'installazione amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c29cbec604ae18745348a62f147d13d2ccbf06c0620b3a5dcca7c6c009045b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105441"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Applicazione di un pacchetto patch a un'installazione amministrativa

È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000.msp creata in [Generazione di](generating-a-patch-package.md)un pacchetto patch . L'aggiornamento può quindi essere propagato agli utenti richiedendo di reinstallare l'applicazione dalla nuova immagine di origine amministrativa.

Un amministratore può usare la riga di comando seguente per aggiornare l'immagine di origine amministrativa che si trova in //server/MNP2000.msi a una nuova immagine di origine uguale a quella che verrebbe prodotta da un'installazione amministrativa da un CD-ROM completamente aggiornato.

**msiexec /a //server/MNP2000.msi /p MNP2000.msp**

I membri del gruppo di lavoro che usano MNP2000 devono reinstallare l'applicazione dalla nuova immagine di origine amministrativa per ricevere l'aggiornamento.

Per reinstallare completamente le applicazioni e memorizzare nella cache il file .msi aggiornato nel computer dell'utente, gli utenti possono immettere uno dei comandi seguenti.

**msiexec /fvomus //server/MNP2000.msi**

**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**

Per reinstallare solo la funzionalità Concert aggiornata e memorizzare nella cache il file .msi aggiornato nel computer dell'utente, gli utenti possono immettere il comando seguente.

**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**

## <a name="next-example"></a>Esempio successivo

[Esempio di localizzazione](a-localization-example.md)

 

 



