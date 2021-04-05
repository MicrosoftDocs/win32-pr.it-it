---
description: Un piccolo aggiornamento può essere applicato a un'applicazione applicando patch all'installazione locale dell'applicazione.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967285"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto

Un piccolo aggiornamento può essere applicato a un'applicazione applicando patch all'installazione locale dell'applicazione.

**Per applicare una patch di aggiornamento di piccole dimensioni a un'installazione locale del prodotto**

1.  Avviare l'installazione della patch dalla riga di comando o usando un eseguibile. Per avviare dalla riga di comando, usare **msiexec/p patch. msp REINSTALL \[ =**_feature list_ *_\] REINSTALLMODE = omus_*. Per avviare da un eseguibile, chiamare [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o il [**Metodo ApplyPatch**](installer-applypatch.md) e fornire gli stessi argomenti della riga di comando.
2.  Quando si applica una patch a un'installazione client, il programma di installazione ignora l'origine dell'installazione e procede con la patch dei file già installati nel computer dell'utente.
3.  Il programma di installazione modifica tutti i componenti patch contrassegnati come Run-from-source per l'esecuzione in locale. Gli utenti non sono in grado di eseguire questi componenti dall'origine a condizione che la patch rimanga nel computer.
4.  Il programma di installazione aggiunge qualsiasi trasformazione utilizzata per aggiornare il file con estensione msi o aggiunge informazioni specifiche della patch al profilo dell'utente.
5.  Il programma di installazione memorizza nella cache il file con estensione msi nel computer dell'utente, in modo da poter eseguire l'installazione su richiesta, reinstallare e ripristinare l'applicazione. Dopo che una patch è stata applicata a un'installazione autonoma, il programma di installazione fa riferimento a due o più elenchi di origine a file esterni: uno per l'origine originale e uno per ogni patch che è stata applicata.

 

 



