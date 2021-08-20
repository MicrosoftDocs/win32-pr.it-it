---
description: Illustra le attività che devono essere eseguite per creare un messaggio firmato.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Creazione di un messaggio firmato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645509c140168267bf48915f68a884b51dee6e7f5a19b2a153e3fd6ff7d5afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769249"
---
# <a name="creating-a-signed-message"></a>Creazione di un messaggio firmato

La figura seguente illustra le attività che devono essere eseguite per creare un messaggio firmato. I passaggi sono elencati di seguito.

![firma di un messaggio](images/signdmsg.png)

**Per creare un messaggio firmato**

1.  Creare i dati (se necessario) e ottenere un puntatore a esso.
2.  Aprire un [*archivio certificati*](../secgloss/c-gly.md) contenente il certificato del firmatario.
3.  Ottenere la [*chiave privata*](../secgloss/p-gly.md) per il certificato. È necessario impostare una proprietà sul certificato prima di usarlo, per associare un certificato a un [*CSP*](../secgloss/c-gly.md)specifico e, all'interno di tale CSP, a una chiave privata specifica. Questa opzione deve essere impostata una sola volta.
4.  Scegliere un algoritmo hash per l'operazione digest. È consigliabile selezionare l'algoritmo hash da una posizione configurabile che può essere successivamente aggiornata senza richiedere modifiche al codice.
5.  Inviare i dati tramite la funzione hash usando l'algoritmo hash, creando così un [*hash*](../secgloss/h-gly.md) (digest) dei dati.
6.  Usando la [*chiave privata*](../secgloss/p-gly.md) ottenuta tramite la proprietà nel certificato, crittografare il digest, creando la firma.
7.  Includere quanto segue nel messaggio firmato:

    -   Dati firmati
    -   Algoritmo hash
    -   Firma
    -   Identificatore del firmatario (autorità di certificazione e numero di serie)
    -   Certificato del firmatario (facoltativo)

Per una procedura dettagliata e un esempio, vedere [Procedura per](procedure-for-signing-data.md) la firma dei dati e Programma C di esempio: firma di un messaggio e Verifica di una firma [del messaggio.](example-c-program-signing-a-message-and-verifying-a-message-signature.md)

 

 
