---
description: Rappresentazione del dispositivo
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Rappresentazione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484740"
---
# <a name="device-representation"></a>Rappresentazione del dispositivo

I dispositivi hanno due comportamenti principali che vengono risolti dall'architettura dei dispositivi portatili Windows (WPD):

-   Accesso e archiviazione del contenuto. Ad esempio, le applicazioni devono essere in grado di aggiungere file musicali a un lettore musicale portatile.
-   Programmazione del dispositivo. Sono incluse operazioni semplici come la modifica delle impostazioni e la preparazione del dispositivo per l'acquisizione dei dati o operazioni più complesse, ad esempio il caricamento del firmware. Gli esempi includono l'esecuzione di un comando "Take picture" in una fotocamera digitale ancora.

In WPD questi comportamenti vengono descritti rappresentando il dispositivo come una gerarchia di oggetti. La figura seguente mostra una rappresentazione dell'oggetto WPD per un dispositivo multifunzione, che in questo caso è un telefono cellulare.

![illustrazione che mostra la gerarchia di oggetti per un telefono cellulare](images/wpd-overview-figure3.gif)

Questa gerarchia illustra le funzionalità e i contenuti seguenti.

Funzionalità

-   Oggetto di archiviazione. Questo dispositivo dispone di archiviazione dati.
-   Servizio contatti. Questo servizio è un oggetto funzionale che può essere utilizzato per sincronizzare e archiviare contatti sul telefono.
-   Servizio SMS. Questo servizio è un oggetto funzionale che può essere utilizzato per l'invio, la ricezione e l'archiviazione di messaggi SMS.

Contenuto:

-   Oggetti multimediali. Questo dispositivo archivia immagini, musica e file video in cartelle nell'oggetto di archiviazione. Mentre i file mostrati nell'illustrazione sono archiviati in una cartella, un dispositivo può suddividere il contenuto in cartelle organizzate in base al tipo di supporto archiviato; ad esempio, cartelle immagini, cartelle musica e cartelle video.
-   Contattare gli oggetti. Questo dispositivo archivia le informazioni di contatto, ad esempio nome, numero di telefono e indirizzo, come elementi figlio del servizio contatti
-   Oggetti Message. Questo dispositivo archivia i messaggi SMS come elementi figlio del servizio SMS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



