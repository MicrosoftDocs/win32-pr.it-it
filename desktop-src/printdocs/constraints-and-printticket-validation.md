---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Vincoli e convalida PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103968996"
---
# <a name="constraints-and-printticket-validation"></a>Vincoli e convalida PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Come descritto nella sezione Schema PrintCapabilities, alcuni dei possibili risultati della configurazione espressi in un documento PrintCapabilities non sono validi per il dispositivo. Le configurazioni non valide sono definite conflitti di vincolo (un termine usato nel mondo dei file PPD/GPD). Per evitare conflitti di vincolo, i provider PrintTicket devono supportare un'operazione di convalida PrintTicket utilizzata dai client per eseguire la convalida sul relativo PrintTicket. Questa operazione dovrebbe rilevare se la configurazione specificata può essere eseguita nel dispositivo. Se non è possibile eseguire la configurazione (poiché gli elementi Feature e Option specificati non esistono nel dispositivo corrente o perché la configurazione è vincolata), l'operazione deve modificare l'oggetto PrintTicket di input in modo che contenga impostazioni valide e non vincolate. L'operazione potrebbe rimuovere o convalidare altre informazioni anche nel PrintTicket. Si noti che quando viene rilevato un conflitto di vincoli, il codice di convalida deve modificare l'impostazione di uno degli attributi del dispositivo per evitare il conflitto di vincoli. Le [definizioni delle opzioni](option-definitions.md) indicano che è necessario usare un processo di assegnazione dei punteggi definito da un driver di dispositivo per determinare quale attributo del dispositivo deve essere modificato, in modo da conservare al meglio la finalità originale dell'utente. Il codice di convalida potrebbe impostare come hardcoded il processo di assegnazione dei punteggi per favorire un attributo del dispositivo rispetto a un altro oppure può utilizzare le informazioni fornite da una particolare istanza di proprietà nell'oggetto PrintTicket per guidare la risoluzione. Poiché nelle parole chiave dello schema di stampa non è definita alcuna proprietà che consente ai client di specificare la priorità relativa di ogni attributo del dispositivo, gli eventuali elementi della proprietà PrintTicket privati utilizzati per questo scopo possono essere ignorati da altri provider PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



