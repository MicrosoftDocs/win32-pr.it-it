---
description: È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000. msp creata in generazione di un pacchetto di patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Applicazione di un pacchetto di patch a un'installazione amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967288"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Applicazione di un pacchetto di patch a un'installazione amministrativa

È possibile applicare il piccolo aggiornamento a un'immagine di origine amministrativa di MNP2000.msi installando la patch di esempio MNP2000. msp creata in [generazione di un pacchetto di patch](generating-a-patch-package.md). L'aggiornamento può quindi essere propagato agli utenti richiedendo la reinstallazione dell'applicazione dalla nuova immagine di origine amministrativa.

Un amministratore può usare la riga di comando seguente per aggiornare l'immagine di origine amministrativa situata in//server/MNP2000.msi a una nuova immagine di origine che corrisponde a quella generata da un'installazione amministrativa da un CD-ROM completamente aggiornato.

**msiexec/a//server/MNP2000.msi/p MNP2000. msp**

I membri del gruppo di lavoro che usa MNP2000 devono reinstallare l'applicazione dalla nuova immagine di origine amministrativa per ricevere l'aggiornamento.

Per reinstallare completamente le applicazioni e memorizzare nella cache il file con estensione msi aggiornato nel computer dell'utente, è possibile che gli utenti immettano uno dei comandi seguenti.

**msiexec/fvomus//server/MNP2000.msi**

**msiexec/I//server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**

Per reinstallare solo la funzionalità di concerto aggiornata e memorizzare nella cache il file con estensione msi aggiornato nel computer dell'utente, è possibile che gli utenti immettano il comando seguente.

**msiexec/I//server/MNP2000.msi REINSTALL = Concert REINSTALLMODE = vomus**

## <a name="next-example"></a>Esempio successivo

[Esempio di localizzazione](a-localization-example.md)

 

 



