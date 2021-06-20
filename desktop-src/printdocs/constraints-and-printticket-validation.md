---
description: Per evitare conflitti di vincoli, i provider PrintTicket devono supportare la convalida utilizzata dai client per eseguire la convalida in PrintTicket.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Vincoli e convalida PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08abc07f0ef96e94720f8f9431a192e5dbcac669
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409574"
---
# <a name="constraints-and-printticket-validation"></a>Vincoli e convalida PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Come illustrato nella sezione Schema PrintCapabilities, alcuni dei possibili risultati della configurazione espressi in un documento PrintCapabilities non sono validi per il dispositivo. Si dice che le configurazioni non valide contengano conflitti di vincolo (termine usato nel mondo dei file PPD/GPD). Per evitare conflitti di vincoli, i provider PrintTicket devono supportare un'operazione di convalida PrintTicket utilizzata dai client per eseguire la convalida in PrintTicket. Questa operazione deve rilevare se la configurazione specificata può verificarsi nel dispositivo. Se la configurazione non può verificarsi (perché gli elementi Feature e Option specificati non esistono nel dispositivo corrente o perché la configurazione è vincolata), l'operazione deve modificare l'input PrintTicket in modo che contenga impostazioni valide e senza vincoli. L'operazione potrebbe rimuovere o convalidare anche altre informazioni in PrintTicket. Si noti che quando viene rilevato un conflitto di vincoli, il codice di convalida deve modificare l'impostazione di uno degli attributi del dispositivo per evitare il conflitto di vincoli. [Le definizioni](option-definitions.md) delle opzioni indicano che è necessario usare un processo di assegnazione dei punteggi definito dal driver di dispositivo per determinare quale attributo del dispositivo deve essere modificato per mantenere al meglio la finalità originale dell'utente. Il codice di convalida potrebbe impostare come hardcoded il processo di assegnazione dei punteggi per favorire un attributo del dispositivo rispetto a un altro oppure potrebbe usare le informazioni fornite da una particolare istanza property in PrintTicket per guidare la risoluzione. Poiché nelle parole chiave dello schema di stampa non è definita alcuna proprietà che consenta ai client di specificare la priorità relativa di ogni attributo del dispositivo, è probabile che gli elementi privati della proprietà PrintTicket usati a questo scopo siano ignorati da altri provider PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



