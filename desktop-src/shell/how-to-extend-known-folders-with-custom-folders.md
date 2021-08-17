---
description: I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando cartelle note proprie.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Come estendere cartelle note con cartelle personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a04a5ef10c8e3ee909944e6782cf32ca6aa2aa6b50e03f018f31a6aafe529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350871"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Come estendere cartelle note con cartelle personalizzate

I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando cartelle note proprie. Dopo la registrazione, queste cartelle di terze parti sono note al sistema. Vengono trovati da qualsiasi chiamata a [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Si noti che una cartella nota deve essere una cartella per computer. Non è possibile creare una cartella nota per utente.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Definire la cartella nota tramite una [**struttura KNOWNFOLDER \_ DEFINITION.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition)

### <a name="step-2"></a>Passaggio 2:

Registrare la cartella nota tramite una chiamata a [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Commenti

Se si crea una cartella nota per l'applicazione come parte della procedura di installazione, è necessario includere [**anche IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) come parte del codice di disinstallazione.

Considerare il motivo per cui si vuole che la cartella venga inclusa nel sistema di cartelle note prima di registrarla. È necessario avere un motivo valido per elevare la cartella a tale livello di visibilità del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
