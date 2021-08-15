---
title: Uso dei buffer di stringa
description: Le funzioni che restituiscono stringhe contengono un parametro di input, lpszBuffer, e un parametro size, lpdwBufferLength. Anche se lpszBuffer può essere NULL, lpdwBufferLength deve essere un puntatore valido a una variabile DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15750da215267a4922bb0cd8c5dd8c08f77e1874af75fb9a671f9ef4cb1f0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413153"
---
# <a name="using-string-buffers"></a>Uso dei buffer di stringa

Le funzioni che restituiscono stringhe contengono un parametro di input, *lpszBuffer,* e un parametro size, *lpdwBufferLength.* Anche *se lpszBuffer* può essere **NULL,** *lpdwBufferLength* deve essere un puntatore valido a una **variabile DWORD.** Se il buffer di input a cui *punta lpszBuffer* è **NULL** o troppo piccolo per contenere la stringa di output, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER**. La variabile a cui punta *lpdwBufferLength* contiene un numero che rappresenta il numero di byte richiesti dalla funzione per restituire la stringa richiesta, incluso il terminatore **Null.** L'applicazione deve allocare un buffer di queste dimensioni, impostare la variabile a cui *punta lpdwBufferLength* su questo valore e inviare nuovamente la richiesta. Se le dimensioni del buffer sono sufficienti per ricevere la stringa richiesta, la stringa viene copiata nel buffer di output con un terminatore **Null** e la funzione restituisce un'indicazione di esito positivo. La variabile a cui punta *lpdwBufferLength* contiene ora il numero di caratteri archiviati nel buffer, escluso il carattere **di terminazione** Null.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 