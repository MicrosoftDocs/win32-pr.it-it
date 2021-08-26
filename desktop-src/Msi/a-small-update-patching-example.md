---
description: In questo esempio viene illustrato come creare un pacchetto di patch che applica un piccolo aggiornamento al pacchetto di installazione di esempio descritto in An Installation Example.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Esempio di applicazione di patch per gli aggiornamenti di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082971"
---
# <a name="a-small-update-patching-example"></a>Esempio di applicazione di patch per gli aggiornamenti di piccole dimensioni

In questo esempio viene illustrato come creare [](small-updates.md) un pacchetto [di patch](patch-packages.md) che applica un piccolo aggiornamento al pacchetto di installazione di esempio descritto in An [Installation Example](an-installation-example.md). Un piccolo aggiornamento apporta modifiche a uno o più file dell'applicazione che sono stati valutati come troppo secondari per garantire la modifica del codice del prodotto. Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)

Questo esempio illustra come creare un pacchetto di patch del programma di installazione di Windows che aggiorna la funzionalità Concert dell'ipotetico prodotto MNP2000 per correggere un errore nel prodotto originale. Il pacchetto patch di esempio applica un piccolo aggiornamento al prodotto che non richiede la modifica del codice del prodotto. Per altre informazioni sugli [aggiornamenti principali,](major-upgrades.md) vedere l'argomento relativo ai principali aggiornamenti nella sezione [Patching and Upgrades](patching-and-upgrades.md) (Applicazione di patch e aggiornamenti).

Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:

-   Corregge un errore secondario nella pianificazione Concert visualizzata dalla funzionalità Concert.
-   Aggiorna il codice del pacchetto in modo da riflettere che il pacchetto di installazione è stato modificato.
-   Il piccolo aggiornamento può essere applicato tramite l'applicazione di patch all'installazione locale del prodotto.

[Continua](planning-a-small-update-patch.md)

 

 



