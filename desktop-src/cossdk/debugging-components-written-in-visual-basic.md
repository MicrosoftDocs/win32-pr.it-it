---
description: Debug di componenti scritti in Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Debug di componenti scritti in Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305223"
---
# <a name="debugging-components-written-in-visual-basic"></a>Debug di componenti scritti in Visual Basic

È possibile utilizzare l'ambiente di sviluppo Microsoft Visual Basic 6,0 per il debug in determinati scenari. L'uso di Visual Basic per il debug consente l'accesso a strumenti familiari con Visual Basic programmatori. D'altra parte, poiché durante il debug Visual Basic componenti vengono eseguiti nel processo dell'ambiente Visual Basic, potrebbe essere necessario eseguire il debug del componente dopo che è stato compilato tramite l'ambiente di sviluppo di Microsoft Visual C++.

Per ulteriori informazioni sul debug all'interno del Visual Basic Integrated Development Environment (IDE), vedere [debug nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md). Per altre informazioni sul debug dei componenti di Visual Basic dopo che sono stati compilati usando l'ambiente di sviluppo Visual C++, vedere [debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md).

Inoltre, per COM+ sono state risolte diverse limitazioni associate all'utilizzo dell'ambiente Visual Basic per eseguire il debug dei componenti con MTS. Per ulteriori informazioni, vedere [COM+ Visual Basic il supporto per il debug in contrapposizione a MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> Se si è già utilizzato Visual Basic nello stesso computer di COM+, è possibile che sia stato notato il componente aggiuntivo Servizi componenti disponibile nell'ambiente Visual Basic. Originariamente in MTS, questa funzionalità è stata progettata per aggiornare il registro di sistema ogni volta che si ricompila un componente in un'applicazione COM+. Tuttavia, data la natura dell'interazione tra il registro di sistema di Microsoft Windows e il database di registrazione COM+, alcune impostazioni potrebbero non essere completamente aggiornate. Pertanto, anziché usare i comandi disponibili con questo componente aggiuntivo, è necessario rimuovere e reinstallare i componenti per aggiornare le impostazioni dopo la ricompilazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di componenti scritti in Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



