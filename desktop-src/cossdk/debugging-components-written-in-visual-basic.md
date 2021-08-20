---
description: Debug di componenti scritti in Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Debug di componenti scritti in Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991181"
---
# <a name="debugging-components-written-in-visual-basic"></a>Debug di componenti scritti in Visual Basic

È possibile usare l'ambiente di sviluppo Microsoft Visual Basic 6.0 per il debug in determinati scenari. L'Visual Basic per il debug consente l'accesso a strumenti familiari Visual Basic programmatori. D'altra parte, poiché durante il debug i componenti Visual Basic vengono eseguiti all'interno del processo dell'ambiente Visual Basic, potrebbe essere necessario eseguire il debug del componente dopo che è stato compilato usando l'ambiente di sviluppo Microsoft Visual C++.

Per altre informazioni sul debug all'interno dell Visual Basic ide (Integrated Development Environment), vedere [Debug nell'IDE Visual Basic .](debugging-in-the-visual-basic-ide.md) Per altre informazioni sul debug Visual Basic componenti dopo che sono stati compilati usando l'ambiente di sviluppo Visual C++, vedere Debug di componenti Visual Basic [compilati.](debugging-compiled-visual-basic-components.md)

Inoltre, sono state risolte diverse limitazioni associate all'uso dell'Visual Basic per eseguire il debug dei componenti con MTS per COM+. Per altre informazioni, vedere [Supporto del debug Visual Basic COM+ in contrasto con MTS.](com--visual-basic-debugging-support-contrasted-with-mts.md)

> [!Note]  
> Se è già stato usato Visual Basic nello stesso computer di COM+, è possibile che si sia notato che il componente aggiuntivo Servizi componenti è disponibile nell'ambiente Visual Basic. Originariamente in MTS, questa funzionalità era progettata per aggiornare il Registro di sistema ogni volta che si ricompilava un componente in un'applicazione COM+. Tuttavia, data la natura dell'interazione del Registro di sistema di Microsoft Windows e del database di registrazione COM+, alcune impostazioni potrebbero non essere completamente aggiornate. Pertanto, anziché usare i comandi disponibili con questo componente aggiuntivo, è necessario rimuovere e reinstallare i componenti per aggiornare le impostazioni dopo la ricompilazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di componenti scritti in Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



