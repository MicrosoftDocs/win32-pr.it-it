---
description: Un nome di simbolo decorato include caratteri che distinguono il modo in cui un simbolo pubblico è stato dichiarato.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nomi di simboli decorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482732"
---
# <a name="decorated-symbol-names"></a>Nomi di simboli decorati

Un nome di simbolo decorato include caratteri che distinguono il modo in cui un simbolo pubblico è stato dichiarato. Per le \_ \_ funzioni stdcall, i nomi includono il carattere "@" e un numero decimale che specifica il numero di byte nei parametri della funzione. Ad esempio, il nome decorato della funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) è LoadLibrary@4 . Per le funzioni C++ la decorazione del nome è più complessa e varia da compilatore a compilatore.

Per recuperare il nome del simbolo non decorato, usare la funzione [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) . In alternativa, è possibile chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per richiedere che il gestore di simboli presenti sempre simboli con nomi non decorati. È necessario impostare questa opzione prima di caricare i simboli perché il gestore di simboli crea le tabelle dei nomi di simboli in fase di caricamento.

 

 
