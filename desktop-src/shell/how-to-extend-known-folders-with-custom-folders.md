---
description: I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando le cartelle note.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Come estendere le cartelle note con cartelle personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227436"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Come estendere le cartelle note con cartelle personalizzate

I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando le cartelle note. Una volta registrate, le cartelle di terze parti sono note al sistema. Vengono rilevate da qualsiasi chiamata a [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Si noti che una cartella nota deve essere una cartella per computer. Non è possibile creare una cartella nota per singolo utente.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Definire la cartella nota tramite una struttura di [**\_ definizione cartellanota**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .

### <a name="step-2"></a>Passaggio 2:

Registrare la cartella nota tramite una chiamata a [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Commenti

Se si crea una cartella nota per l'applicazione come parte della procedura di installazione, è necessario includere anche [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) come parte del codice di disinstallazione.

Tenere in considerazione i motivi per cui si desidera che la cartella venga inclusa nel sistema di cartelle note prima di registrarla. È necessario avere un motivo valido per elevare la cartella a tale livello di visibilità del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
