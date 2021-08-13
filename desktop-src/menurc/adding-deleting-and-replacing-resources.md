---
title: Aggiunta, eliminazione e sostituzione di risorse
description: In questo argomento viene illustrato come aggiungere, eliminare o sostituire risorse.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c23375dbfff770a22b96ef7cb517af1c0b8d40579d6919a31a8136e1691474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735294"
---
# <a name="adding-deleting-and-replacing-resources"></a>Aggiunta, eliminazione e sostituzione di risorse

Le applicazioni devono spesso aggiungere, eliminare o sostituire risorse nei file eseguibili. Per eseguire queste attività, è possibile usare due metodi. Il primo è modificare il file di definizione delle risorse, ricompilare le risorse e aggiungere le risorse ricompilate al file eseguibile dell'applicazione. Il secondo metodo è copiare i dati delle risorse direttamente nel file eseguibile dell'applicazione.

Ad esempio, per localizzare un'applicazione in lingua inglese per l'uso in Norvegia, potrebbe essere necessario sostituire la finestra di dialogo Inglese con una usando il norvegese. Uno sviluppatore crea una finestra di dialogo appropriata usando un editor di finestre di dialogo o scrivendo un modello nel file di definizione delle risorse. Lo sviluppatore ricompila quindi le risorse e aggiunge le nuove risorse al file eseguibile dell'applicazione.

Se tuttavia esiste una finestra di dialogo appropriata in formato binario, lo sviluppatore può copiare i dati direttamente nel file eseguibile localizzato usando le funzioni seguenti. La [**funzione BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) crea un handle di aggiornamento per il file eseguibile le cui risorse devono essere modificate. La [**funzione UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa questo handle per aggiungere, eliminare o sostituire una risorsa nel file eseguibile. La [**funzione EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) chiude l'handle.

Dopo aver creato un handle di aggiornamento per un file eseguibile da [**BeginUpdateResource,**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)un'applicazione può usare [**Ripetutamente UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) per apportare modifiche ai dati delle risorse. Ogni chiamata **a UpdateResource** contribuisce a un elenco interno di aggiunte, eliminazioni e sostituzioni, ma non scrive effettivamente i dati nel file eseguibile. Immediatamente prima di chiudere l'handle di aggiornamento, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) scrive le modifiche accumulate nel file eseguibile.

In alcuni casi, un'applicazione deve copiare le risorse da un altro file. [L'aggiornamento](using-resources.md) delle risorse mostra un esempio di come ottenere i dati delle risorse e le relative dimensioni da un file.

 

 




