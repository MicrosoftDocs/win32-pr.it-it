---
description: Questo esempio illustra come creare un pacchetto di patch che applica un piccolo aggiornamento al pacchetto di installazione di esempio descritto in un esempio di installazione.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Un piccolo esempio di patch di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311101"
---
# <a name="a-small-update-patching-example"></a>Un piccolo esempio di patch di aggiornamento

Questo esempio illustra come creare un pacchetto di [patch](patch-packages.md) che applica un [piccolo aggiornamento](small-updates.md) al pacchetto di installazione di esempio descritto in [un esempio di installazione](an-installation-example.md). Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione giudicati troppo piccoli per garantire la modifica del codice del prodotto. Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).

Questo esempio illustra come creare un pacchetto di patch Windows Installer che aggiorna la funzionalità di concerto del prodotto ipotetico MNP2000 per correggere un errore nel prodotto originale. Il pacchetto di patch di esempio applica un piccolo aggiornamento al prodotto che non richiede la modifica del codice del prodotto. Per ulteriori informazioni sugli aggiornamenti principali, vedere l'argomento relativo agli [aggiornamenti principali](major-upgrades.md) nella sezione applicazione di [patch e aggiornamenti](patching-and-upgrades.md) .

Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:

-   Corregge un errore secondario nella pianificazione del concerto visualizzata dalla funzionalità Concert.
-   Aggiorna il codice del pacchetto in modo da riflettere che il pacchetto di installazione è stato modificato.
-   Il piccolo aggiornamento può essere applicato applicando patch all'installazione locale del prodotto.

[Continua](planning-a-small-update-patch.md)

 

 



