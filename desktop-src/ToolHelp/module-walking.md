---
title: Module Walking
description: Uno snapshot che include l'elenco di moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), usata dal processo specificato.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- librerie a collegamento dinamico
- librerie a collegamento dinamico, enumerazione di DLL
- enumerazione
- enumerazione, DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61e72fcdbcae52a78e62465b12845077572b6b4669e1b0744c26d50ddfd2a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126491"
---
# <a name="module-walking"></a>Module Walking

Uno snapshot che include l'elenco di moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), usata dal processo specificato. È possibile recuperare informazioni per il primo modulo nell'elenco usando la [**funzione Module32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) Dopo aver recuperato il primo modulo nell'elenco, è possibile recuperare le informazioni per i moduli successivi nell'elenco usando la [**funzione Module32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) **Module32First** e **Module32Next** compilano una [**struttura MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con informazioni sul modulo.

È possibile recuperare un codice di stato di errore esteso per [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) usando la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> L'identificatore del modulo, specificato nel membro **th32ModuleID** di [**MODULEENTRY32,**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)ha un significato solo nelle classi a 16 bit Windows.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'elenco di moduli](traversing-the-module-list.md)
</dt> </dl>

 

 