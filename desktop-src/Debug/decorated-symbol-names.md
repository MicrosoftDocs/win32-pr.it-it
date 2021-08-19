---
description: Un nome di simbolo decorato include caratteri che distinguono la modalità di dichiarazione di un simbolo pubblico.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nomi di simboli decorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60432788b69f0c8779030f32a190ccfb55859434f714a13f769b328ee246a309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076415"
---
# <a name="decorated-symbol-names"></a>Nomi di simboli decorati

Un nome di simbolo decorato include caratteri che distinguono la modalità di dichiarazione di un simbolo pubblico. Per \_ le funzioni stdcall, i nomi includono il carattere "@" e un numero decimale che specifica \_ il numero di byte nei parametri della funzione. Ad esempio, il nome decorato della [**funzione LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) è LoadLibrary@4 . Per le funzioni C++, la decorazione dei nomi è più complessa e varia da compilatore a compilatore.

Per recuperare il nome del simbolo non dichiarato, usare la [**funzione UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) In alternativa, è possibile chiamare la [**funzione SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per richiedere che il gestore dei simboli presenti sempre simboli con nomi non dichiarati. È necessario impostare questa opzione prima di caricare i simboli perché il gestore dei simboli crea le tabelle dei nomi dei simboli in fase di caricamento.

 

 
