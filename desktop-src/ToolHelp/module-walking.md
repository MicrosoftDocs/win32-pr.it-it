---
title: Esplorazione del modulo
description: Uno snapshot che include l'elenco dei moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), utilizzato dal processo specificato.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- librerie a collegamento dinamico
- librerie a collegamento dinamico, enumerazione di dll
- enumerazione
- Enumerazione, dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117863"
---
# <a name="module-walking"></a>Esplorazione del modulo

Uno snapshot che include l'elenco dei moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), utilizzato dal processo specificato. È possibile recuperare le informazioni per il primo modulo nell'elenco usando la funzione [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . Dopo aver recuperato il primo modulo nell'elenco, è possibile recuperare le informazioni per i moduli successivi nell'elenco usando la funzione [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** e **Module32Next** riempiono una struttura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con informazioni sul modulo.

È possibile recuperare un codice di stato di errore esteso per [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> L'identificatore del modulo, specificato nel membro **th32ModuleID** di [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), ha significato solo in Windows a 16 bit.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'elenco dei moduli](traversing-the-module-list.md)
</dt> </dl>

 

 