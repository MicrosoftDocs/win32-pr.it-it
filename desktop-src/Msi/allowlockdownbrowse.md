---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; consente agli utenti non amministratori di utilizzare una finestra di dialogo Sfoglia per individuare le origini di applicazioni gestite.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881142"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

L'impostazione del valore di questo criterio di [sistema](system-policy.md) per computer su "1" consente agli utenti non amministratori di utilizzare una [finestra di dialogo Sfoglia](browse-dialog.md) per individuare le origini di [*applicazioni gestite*](m-gly.md). Le origini possono includere supporti, ad esempio CD-ROM, URL e percorsi di rete. Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md). Il valore predefinito Windows Installer è che gli utenti non amministratori non possono cercare nuove origini di applicazioni gestite. Le uniche origini disponibili sono quelle già registrate nell'elenco di origine del prodotto. Se questo criterio è impostato, un utente non amministratore potrebbe individuare le nuove origini delle applicazioni assegnate o pubblicate o installate per tutti gli utenti. L'impostazione di AllowLockdownBrowse consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.

L'impostazione predefinita è consigliata per garantire un ambiente protetto.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto di Windows Installer per l'installazione o l'avvio di tali programmi.

[DisableBrowse](disablebrowse.md) esegue l'override di AllowLockdownBrowse e impedisce l'esplorazione anche se è impostato AllowLockdownBrowse.

Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



