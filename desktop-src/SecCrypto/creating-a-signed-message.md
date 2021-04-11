---
description: Descrive le attività che devono essere eseguite per creare un messaggio firmato.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Creazione di un messaggio firmato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232219"
---
# <a name="creating-a-signed-message"></a>Creazione di un messaggio firmato

Nella figura seguente vengono illustrate le attività che devono essere eseguite per creare un messaggio firmato. I passaggi sono elencati dopo l'illustrazione.

![firma di un messaggio](images/signdmsg.png)

**Per creare un messaggio firmato**

1.  Creare i dati (se necessario) e ottenere un puntatore.
2.  Aprire un [*archivio certificati*](../secgloss/c-gly.md) che contiene il certificato del firmatario.
3.  Ottenere la [*chiave privata*](../secgloss/p-gly.md) per il certificato. Una proprietà deve essere impostata sul certificato prima di utilizzarla, per associare un certificato a un particolare [*CSP*](../secgloss/c-gly.md)e, all'interno di tale CSP, a una chiave privata specifica. Questa operazione deve essere impostata una sola volta.
4.  Scegliere un algoritmo di hash per l'operazione digest. Si consiglia di selezionare l'algoritmo hash da un percorso configurabile che può essere successivamente aggiornato senza richiedere modifiche al codice.
5.  Inviare i dati tramite la funzione hash usando l'algoritmo hash, creando in tal modo un [*hash*](../secgloss/h-gly.md) (digest) dei dati.
6.  Utilizzando la [*chiave privata*](../secgloss/p-gly.md) ottenuta tramite la proprietà del certificato, crittografare il digest e creare la firma.
7.  Includere quanto segue nel messaggio firmato:

    -   Dati firmati
    -   Algoritmo hash
    -   Firma
    -   Identificatore del firmatario (autorità emittente del certificato e numero di serie)
    -   Il certificato del firmatario (facoltativo)

Per una procedura dettagliata e un esempio, vedere la [procedura per la firma di dati](procedure-for-signing-data.md) e [il programma C di esempio: firma di un messaggio e verifica della firma di un messaggio](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
