---
title: Informazioni sul modulo
description: Un modulo è un file eseguibile o una DLL.
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399132"
---
# <a name="module-information"></a>Informazioni sul modulo

Un *modulo* è un file eseguibile o una dll. Ogni processo è costituito da uno o più moduli. È possibile recuperare l'elenco di handle di modulo per un processo chiamando la funzione [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) . Questa funzione riempie una matrice di valori **hmodule** con gli handle del modulo per il processo specificato. Il primo modulo è il file eseguibile. Tenere presente che questi handle di modulo sono molto probabilmente da un altro processo, pertanto non è possibile utilizzarli con funzioni come [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea). Tuttavia, è possibile usare le [funzioni PSAPI](psapi-functions.md) per ottenere informazioni su un modulo da un altro processo.

Nella procedura seguente viene descritto come ottenere informazioni sui moduli da un altro processo.

**Per ottenere informazioni sui moduli da un altro processo**

1.  Chiamare la funzione [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) . Questa funzione accetta un handle di processo e un handle del modulo come input e compila un buffer con il nome di base di un modulo, ad esempio Kernel32.dll. Una funzione correlata, [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa), accetta gli stessi parametri di input, ma restituisce il percorso completo del modulo (ad esempio, C: \\ Windows \\ system32 \\Kernel32.dll).
2.  Chiamare la funzione [**GetModuleInformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) . Questa funzione accetta un handle di processo e un handle di modulo e riempie una struttura [**ModuleInfo**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) con l'indirizzo di carico del modulo, la dimensione dello spazio degli indirizzi lineare occupata e un puntatore al relativo punto di ingresso.

Se un'applicazione richiede informazioni sul modulo per il processo corrente, deve usare la funzione [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) anziché le funzioni del modulo PSAPI. Questo consente di migliorare le prestazioni delle applicazioni in due modi: la funzione **GetModuleFileName** è più efficiente delle funzioni del modulo PSAPI e un'applicazione può evitare il caricamento psapi.dll se non usa funzioni PSAPI.

Le funzioni [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) e [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) sono progettate principalmente per l'uso da parte di debugger e applicazioni simili che devono estrarre informazioni sui moduli da un altro processo. Se l'elenco dei moduli nel processo di destinazione è danneggiato o non è stato ancora inizializzato o se l'elenco dei moduli cambia durante la chiamata di funzione in seguito al caricamento o allo scaricamento delle dll, queste funzioni potrebbero non riuscire o restituire informazioni non corrette.

 

 