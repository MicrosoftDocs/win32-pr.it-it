---
description: Un aggiornamento principale può essere applicato a un'applicazione mediante l'applicazione di patch all'installazione locale dell'applicazione dalla riga di comando o tramite un eseguibile.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881126"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto

Un aggiornamento principale può essere applicato a un'applicazione mediante l'applicazione di patch all'installazione locale dell'applicazione dalla riga di comando o tramite un eseguibile.

> [!Note]  
> Non è consigliabile fornire un aggiornamento principale come pacchetto di patch, perché un pacchetto di patch di aggiornamento principale non può essere sequenziato con altri aggiornamenti e perché la patch non è [installabile](uninstallable-patches.md). Non è possibile usare l'utilità [Msimsp.exe](msimsp-exe.md) per generare un pacchetto di patch che applica un aggiornamento principale. In alternativa, applicare gli aggiornamenti principali, come descritto in [applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md).

 

**Per applicare una patch di aggiornamento principale a un'installazione locale del prodotto**

1.  Avviare l'installazione della patch dalla riga di comando o usando un eseguibile. Per avviare dalla riga di comando, usare msiexec/p patch. msp. Per avviare da un eseguibile, chiamare [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o il [**Metodo ApplyPatch**](installer-applypatch.md) e fornire gli stessi argomenti della riga di comando.
2.  Quando si applica una patch a un'installazione client, il programma di installazione ignora l'origine dell'installazione e procede con la patch dei file già installati nel computer dell'utente.
3.  Il programma di installazione modifica tutti i componenti patch contrassegnati come Run-from-source per l'esecuzione in locale. Gli utenti non sono in grado di eseguire questi componenti dall'origine a condizione che la patch rimanga nel computer.
4.  Il programma di installazione aggiunge qualsiasi trasformazione utilizzata per aggiornare il file con estensione msi o aggiunge informazioni specifiche della patch al profilo dell'utente.
5.  Il programma di installazione memorizza nella cache il file con estensione msi nel computer dell'utente, in modo da poter eseguire l'installazione su richiesta, reinstallare e ripristinare l'applicazione. Dopo che una patch è stata applicata a un'installazione autonoma, il programma di installazione fa riferimento a due o più elenchi di origine a file esterni: uno per l'origine originale e uno per ogni patch che è stata applicata.

 

 



