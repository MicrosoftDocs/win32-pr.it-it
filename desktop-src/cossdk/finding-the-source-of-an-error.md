---
description: Individuazione dell'origine di un errore
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Individuazione dell'origine di un errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049259"
---
# <a name="finding-the-source-of-an-error"></a>Individuazione dell'origine di un errore

È possibile diagnosticare l'origine e ottenere una descrizione degli errori dell'applicazione utilizzando COM+ e altri strumenti. Se si rileva che l'errore dell'applicazione è causato da COM+, è possibile interpretare il messaggio di errore visualizzando il file Winerror. h o utilizzando l'utilità Microsoft Visual C++ Error.

Se l'applicazione server non riesce o causa un comportamento imprevisto, è necessario innanzitutto determinare dove si è verificato l'errore. Il sistema Visualizzatore eventi tiene traccia degli eventi dell'applicazione, della sicurezza e del sistema. Molti errori "invisibile" vengono registrati qui. Tuttavia, non tutti gli errori vengono visualizzati nel Visualizzatore eventi.

Prima di tutto, è necessario fare riferimento al registro applicazioni nel Visualizzatore eventi per controllare l'applicazione associata al messaggio di evento. Poiché è inoltre possibile archiviare i registri eventi, è possibile tenere traccia di una cronologia eventi dell'errore. Se si fa doppio clic su una voce nel log, viene attivata una pagina **Proprietà evento** che fornisce ulteriori informazioni sull'evento di sistema.

Per ulteriori informazioni sul debug di un'applicazione COM+, vedere [debug di applicazioni com+](debugging-com--applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



