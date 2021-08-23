---
description: Denominazione dei mailslot e inserimento dei messaggi in mailslot.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomi di Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f96cc5300b3472abe7d6e824266bd0abd0e7b668e38f9f3462eee3cbf3dfb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716901"
---
# <a name="mailslot-names"></a>Nomi di Mailslot

Quando un processo crea un mailslot, il nome del mailslot deve avere il formato seguente.

\\\\.\\ Nome percorso mailslot \\ \[  \\ \] 

Un nome di mailslot richiede gli elementi seguenti: due barre rovesciate per iniziare il nome, un punto, una barra rovesciata dopo il punto, la parola "mailslot" e una barra rovesciata finale. I nomi non supportano la distinzione tra maiuscole e minuscole. Un nome di mailslot può essere preceduto da un percorso costituito dai nomi di una o più directory, separati da barre rovesciate. Ad esempio, se un utente prevede messaggi sull'oggetto delle imposte da Bob, Pete e Sue, l'applicazione mailslot dell'utente potrebbe consentire all'utente di creare singoli mailslot per ogni mittente, come illustrato di seguito:<dl> \\\\.\\ mailslot \\ taxes \\ bobs \_ comments  
\\\\.\\ commenti di mailslot \\ taxes \\ petes \_  
\\\\.\\ mailslot \\ taxes \\ sues \_ comments  
</dl>

Per inserire un messaggio in un mailslot, un processo apre un mailslot in base al nome. Per scrivere in un mailslot nel computer locale, un processo può usare un nome mailslot con lo stesso formato usato per la creazione di un mailslot. Questa situazione, tuttavia, è relativamente insolita. Più spesso, è necessario usare il formato seguente per scrivere in un mailslot in un computer remoto specifico:

\\\\*Nomecomputer* \\ Nome percorso mailslot \\ \[  \\ \] 

Per inserire un messaggio in ogni mailslot nel dominio specificato con un nome specificato, usare il formato seguente:

\\\\*Nomedominio* \\ Nome percorso mailslot \\ \[  \\ \] 

Per inserire un messaggio in ogni mailslot con un nome specifico nel dominio primario del sistema, usare il formato seguente:

\\\\\*\\Nome percorso mailslot \\ \[  \\ \] 

 

 



