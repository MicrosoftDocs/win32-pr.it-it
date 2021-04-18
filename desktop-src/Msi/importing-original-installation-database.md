---
description: Iniziare la creazione del pacchetto di aggiornamento copiando il pacchetto di installazione e la struttura di directory di origine del prodotto originale.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importazione del database di installazione originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314782"
---
# <a name="importing-original-installation-database"></a>Importazione del database di installazione originale

Iniziare la creazione del pacchetto di aggiornamento copiando il pacchetto di installazione e la struttura di directory di origine del prodotto originale. Le istruzioni per la creazione del pacchetto di installazione per MNP2000 sono fornite in [un esempio di installazione](an-installation-example.md). È necessario copiare il contenuto delle cartelle seguenti:

C: \\MNP2000.msi di esempio \\

C: \\ \\ blocco note di esempio\\

C: \\ \\ file binario di esempio\\

C: \\ icona di esempio \\\\

Aggiornare il contenuto della cartella del blocco note in modo che corrisponda all'origine descritta in [pianificazione di un aggiornamento principale](planning-a-major-upgrade.md). Rimuovere tutti i file di origine obsoleti, ad esempio Baseball.txt, e sostituire con i file aggiornati, ad esempio Baseba01.txt. Aggiungere i nuovi file aggiuntivi forniti dall'aggiornamento, ad esempio Opera01.txt.

Rinominare MNP2000.msi in MNP2001.msi. Nei passaggi successivi si userà un editor tabelle per modificare il database nel file con estensione msi per l'aggiornamento. Le tabelle di database non modificate in modo esplicito nelle sezioni successive sono identiche alle tabelle nel database del prodotto originale, MNP2000.msi.

[Continua](updating-directory-structure-for-an-upgrade.md)

 

 



