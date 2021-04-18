---
title: Aggiunta, eliminazione e sostituzione di risorse
description: In questo argomento viene illustrato come aggiungere, eliminare o sostituire le risorse.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298581"
---
# <a name="adding-deleting-and-replacing-resources"></a>Aggiunta, eliminazione e sostituzione di risorse

Le applicazioni devono spesso aggiungere, eliminare o sostituire le risorse nei file eseguibili. Per eseguire queste attività, è possibile utilizzare due metodi. Il primo consiste nel modificare il file di definizione delle risorse, ricompilare le risorse e aggiungere le risorse ricompilate al file eseguibile dell'applicazione. Il secondo metodo consiste nel copiare i dati della risorsa direttamente nel file eseguibile dell'applicazione.

Per localizzare, ad esempio, un'applicazione in lingua inglese per l'utilizzo in Norvegia, potrebbe essere necessario sostituire la finestra di dialogo inglese con una con il norvegese. Uno sviluppatore crea una finestra di dialogo appropriata utilizzando un editor della finestra di dialogo o scrivendo un modello nel file di definizione delle risorse. Lo sviluppatore ricompila quindi le risorse e aggiunge le nuove risorse al file eseguibile dell'applicazione.

Se una finestra di dialogo appropriata è presente in formato binario, tuttavia, lo sviluppatore può copiare i dati direttamente nel file eseguibile localizzato usando le funzioni seguenti. La funzione [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) crea un handle di aggiornamento per il file eseguibile le cui risorse devono essere modificate. La funzione [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa questo handle per aggiungere, eliminare o sostituire una risorsa nel file eseguibile. La funzione [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) chiude l'handle.

Dopo che un handle di aggiornamento per un file eseguibile viene creato da [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea), un'applicazione può usare [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) ripetutamente per apportare modifiche ai dati della risorsa. Ogni chiamata a **UpdateResource** contribuisce a un elenco interno di aggiunte, eliminazioni e sostituzioni, ma non scrive effettivamente i dati nel file eseguibile. Immediatamente prima di chiudere l'handle di aggiornamento, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) scrive le modifiche accumulate nel file eseguibile.

In alcuni casi, un'applicazione deve copiare le risorse da un altro file. L' [aggiornamento delle risorse](using-resources.md) Mostra un esempio di recupero dei dati delle risorse e delle relative dimensioni da un file.

 

 




