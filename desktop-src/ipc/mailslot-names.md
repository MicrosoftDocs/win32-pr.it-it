---
description: Denominazione di mailslot e inserimento di messaggi in mailslot.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomi inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749687"
---
# <a name="mailslot-names"></a>Nomi inserimento/espulsione

Quando un processo crea un inserimento/espulsione, il nome inserimento/espulsione deve avere il formato seguente.

\\\\.\\ \\ \[  \\ \] *nome* percorso inserimento/espulsione

Un nome inserimento/espulsione richiede gli elementi seguenti: due barre rovesciate per iniziare il nome, un punto, una barra rovesciata che segue il punto, la parola "inserimento/espulsione" e una barra rovesciata finale. I nomi non fanno distinzione tra maiuscole e minuscole. Un nome inserimento/espulsione può essere preceduto da un percorso costituito dai nomi di una o più directory, separate da barre rovesciate. Se, ad esempio, un utente prevede che i messaggi siano soggetti a imposte da Bob, Pete e querela, l'applicazione inserimento/espulsione dell'utente potrebbe consentire all'utente di creare singoli mailslot per ogni mittente, come illustrato di seguito:<dl> \\\\.\\ Commenti su inserimento/espulsione \\ imposte \\ Bob \_  
\\\\.\\ inserimento/espulsione \\ imposte \\ Petes \_  
\\\\.\\ inserimento/espulsione \\ le imposte \\ causa \_ Commenti  
</dl>

Per inserire un messaggio in un inserimento/espulsione, un processo apre un inserimento/espulsione in base al nome. Per scrivere in un inserimento/espulsione nel computer locale, un processo può usare un nome di inserimento/espulsione con lo stesso formato usato per la creazione di un inserimento/espulsione. Questa situazione, tuttavia, è relativamente insolita. Con maggiore frequenza, utilizzare il seguente formato per scrivere in un inserimento/espulsione in un computer remoto specifico:

\\\\*Nomecomputer* \\ \\ \[  \\ \] *nome* percorso inserimento/espulsione

Per inserire un messaggio in ogni inserimento/espulsione del dominio specificato con un nome specificato, utilizzare il formato seguente:

\\\\*NomeDominio* \\ \\ \[  \\ \] *nome* percorso inserimento/espulsione

Per inserire un messaggio in ogni inserimento/espulsione con un nome specificato nel dominio primario del sistema, usare il formato seguente:

\\\\\*\\\\ \[  \\ \] *nome* percorso inserimento/espulsione

 

 



