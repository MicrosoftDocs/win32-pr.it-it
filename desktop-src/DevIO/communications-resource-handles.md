---
description: Un processo utilizza la funzione CreateFile per aprire un handle per una risorsa di comunicazione.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Handle delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401442"
---
# <a name="communications-resource-handles"></a>Handle delle risorse di comunicazione

Un processo utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per una risorsa di comunicazione. Se, ad esempio, si specifica COM1, viene aperto un handle per una porta seriale e LPT1 apre un handle per una porta parallela. Se la risorsa specificata è attualmente in uso da un altro processo, **CreateFile** ha esito negativo. Qualsiasi thread del processo può utilizzare l'handle restituito da **CreateFile** per identificare la risorsa in una qualsiasi delle funzioni che accedono alla risorsa.

Quando il processo chiama [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire una risorsa di comunicazione, specifica gli attributi seguenti:

-   Quale tipo di accesso in lettura/scrittura esiste per la risorsa specificata.
-   Indica se l'handle può essere ereditato dai processi figlio.
-   Indica se l'handle può essere utilizzato nelle operazioni di I/O sovrapposte (asincrone). Per una descrizione delle operazioni sovrapposte, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).

Quando il processo utilizza [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire una risorsa di comunicazione, è necessario specificare determinati valori per i parametri seguenti:

-   Il parametro *fdwShareMode* deve essere zero, aprendo la risorsa per l'accesso esclusivo.
-   Il parametro *fdwCreate* deve specificare il \_ flag aperto esistente.
-   Il parametro *hTemplateFile* deve essere **null**.

Quando si usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle direttamente in un dispositivo, un'applicazione deve usare i caratteri speciali " \\ \\ . \\ " per identificare il dispositivo. Per aprire un handle per l'unità A, ad esempio, specificare \\ \\ . \\ r: per il parametro *lpszName* di **CreateFile**. Il processo chiamante può usare l'handle nella funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare i codici di controllo al dispositivo.

 

 
