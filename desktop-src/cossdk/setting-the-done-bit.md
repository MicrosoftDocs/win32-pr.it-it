---
description: Impostazione del bit done
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Impostazione del bit done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad2d9a9dc06caa623d3f7c58d51aec389b40a1f3315ae09a21052bdf6e2ae3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070251"
---
# <a name="setting-the-done-bit"></a>Impostazione del bit done

COM+ disattiva un oggetto attivato tramite JIT in base allo stato di una proprietà di contesto, il bit done, come indicato di seguito:

-   Quando il bit done è impostato su True, COM+ disattiva l'oggetto quando viene restituita la chiamata al metodo corrente.
-   Quando il bit done è impostato su False, l'oggetto rimane attivo quando viene restituita la chiamata al metodo corrente.

Per impostazione predefinita, il bit done è impostato su False quando viene creato un oggetto e il relativo contesto viene inizializzato. Qualsiasi oggetto attivato tramite JIT viene creato nel proprio contesto in modo che abbia il proprio bit da impostare. Tuttavia, è possibile modificare questa impostazione predefinita in base al metodo usando la proprietà eseguita automaticamente. È possibile impostare il bit done nei modi seguenti:

-   Uso [ **di IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Uso [ **di IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Uso della proprietà auto-done

## <a name="using-icontextstate"></a>Uso di IContextState

È possibile usare [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) per impostare il bit eseguito su True o False.

È possibile usare [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) per ottenere lo stato corrente del bit eseguito dal contesto dell'oggetto.

## <a name="using-iobjectcontext"></a>Uso di IObjectContext

È possibile usare i metodi seguenti in [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) per impostare il bit eseguito impostando contemporaneamente il bit coerente usato per il voto nelle transazioni:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) segnala che l'operazione è stata completata e che si vota per eseguire il commit della transazione corrente. Imposta sia il bit eseguito che il bit coerente su True.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) segnala che l'operazione è stata completata e che la transazione corrente è stata ergasta. Imposta il bit eseguito su True e il bit coerente su False.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) segnala che l'operazione non è stata completata ma che si vota per eseguire il commit della transazione. Imposta il bit eseguito su False e il bit coerente su True.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) segnala che l'operazione non è stata completata e che si vota di non eseguire il commit della transazione in questo momento, in genere perché lo stato è incoerente. Imposta sia il bit eseguito che il bit coerente su False.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pool di oggetti e attivazione JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transazioni e attivazione JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



