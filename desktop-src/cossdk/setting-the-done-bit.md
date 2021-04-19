---
description: Impostazione del bit completato
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Impostazione del bit completato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305131"
---
# <a name="setting-the-done-bit"></a>Impostazione del bit completato

COM+ attiverà un oggetto attivato tramite JIT in base allo stato di una proprietà di contesto, ovvero il bit done, come segue:

-   Quando il bit done è impostato su true, COM+ disattiva l'oggetto quando viene restituita la chiamata al metodo corrente.
-   Quando il bit done è impostato su false, l'oggetto rimane attivo quando viene restituita la chiamata al metodo corrente.

Per impostazione predefinita, il bit done viene impostato su false quando viene creato un oggetto e il relativo contesto viene inizializzato. (Qualsiasi oggetto attivato tramite JIT viene creato nel relativo contesto, in modo da impostare il proprio bit done). Tuttavia, è possibile modificare questa impostazione predefinita in base al metodo usando la proprietà auto-done. È possibile impostare il bit done nei modi seguenti:

-   Uso di [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Uso di [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Uso della proprietà auto-done

## <a name="using-icontextstate"></a>Uso di IContextState

È possibile usare [**IContextState:: setDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) per impostare il bit done su true o false.

È possibile usare [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) per ottenere lo stato corrente del bit fatto dal contesto dell'oggetto.

## <a name="using-iobjectcontext"></a>Uso di IObjectContext

È possibile usare i metodi seguenti in [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) per impostare il bit fatto durante l'impostazione simultanea del bit coerente usato per il voto nelle transazioni:

-   Il [**Secomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) indica che l'operazione è stata completata e che si vota per eseguire il commit della transazione corrente. Imposta sia il bit done sia il bit coerente su true.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) segnala che l'utente ha terminato la transazione corrente. Imposta il bit done su true e il bit coerente su false.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) segnala che non è stato fatto, ma che si vota per eseguire il commit della transazione. Imposta il bit done su false e il bit coerente su true.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) segnala che l'operazione non è stata eseguita e che si vota di non eseguire il commit della transazione in questo momento, in genere perché lo stato è incoerente. Imposta sia il bit done sia il bit coerente su false.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pool di oggetti e attivazione JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transazioni e attivazione JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



