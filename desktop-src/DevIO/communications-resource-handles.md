---
description: Un processo usa la funzione CreateFile per aprire un handle a una risorsa di comunicazione.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Handle di risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585d7ab257c36bc288a494c2e55d9f192749e9742b0eb88ead6d0b0ffad919cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768761"
---
# <a name="communications-resource-handles"></a>Handle di risorse di comunicazione

Un processo usa la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle a una risorsa di comunicazione. Se ad esempio si specifica COM1, viene aperto un handle a una porta seriale e LPT1 apre un handle a una porta parallela. Se la risorsa specificata è attualmente usata da un altro processo, **CreateFile ha** esito negativo. Qualsiasi thread del processo può usare l'handle restituito da **CreateFile** per identificare la risorsa in una qualsiasi delle funzioni che accedono alla risorsa.

Quando il processo chiama [**CreateFile per**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aprire una risorsa di comunicazione, specifica gli attributi seguenti:

-   Tipo di accesso in lettura/scrittura esistente per la risorsa specificata.
-   Indica se l'handle può essere ereditato dai processi figlio.
-   Indica se l'handle può essere usato in operazioni di I/O sovrapposte (asincrone). Per una descrizione delle operazioni sovrapposte, vedere [Sincronizzazione.](/windows/desktop/Sync/synchronization)

Quando il processo usa [**CreateFile per**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aprire una risorsa di comunicazione, deve specificare determinati valori per i parametri seguenti:

-   Il *parametro fdwShareMode* deve essere zero, aprendo la risorsa per l'accesso esclusivo.
-   Il *parametro fdwCreate* deve specificare il flag OPEN \_ EXISTING.
-   Il *parametro hTemplateFile* deve essere **NULL.**

Quando si [**usa CreateFile per**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aprire un handle direttamente a un dispositivo, un'applicazione deve usare i caratteri speciali " \\ \\ . " per identificare \\ il dispositivo. Ad esempio, per aprire un handle per l'unità A, specificare \\ \\ . \\ a: per il *parametro lpszName* di **CreateFile**. Il processo chiamante può usare l'handle nella [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare i codici di controllo al dispositivo.

 

 
