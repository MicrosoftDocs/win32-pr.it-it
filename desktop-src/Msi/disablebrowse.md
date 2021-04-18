---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; impedisce agli utenti non amministratori di utilizzare una finestra di dialogo Sfoglia per individuare le origini di applicazioni gestite archiviate su supporti, ad esempio CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305968"
---
# <a name="disablebrowse"></a>DisableBrowse

Impostando il valore di questo criterio di [sistema](system-policy.md) per computer su "1" si impedisce agli utenti non amministratori di utilizzare una [finestra di dialogo Sfoglia](browse-dialog.md) per individuare le origini di [*applicazioni gestite*](m-gly.md) archiviate su supporti, ad esempio CD-ROM. La casella combinata "utilizza funzionalità da:" per l'input diretto è bloccata e il "Sfoglia". il pulsante è disabilitato. Per altri dettagli sull'esplorazione dell'origine, vedere [resilienza dell'origine](source-resiliency.md).

DisableBrowse esegue l'override di AllowLockdownBrowse e impedisce l'esplorazione anche se è impostato AllowLockdownBrowse.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

In alcuni casi con DisableBrowse impostato, un utente non amministratore potrebbe ancora essere in grado di installare le applicazioni gestite dalle origini nei supporti con etichetta corretta. L'impostazione del criterio DisableBrowse Disabilita solo la possibilità di passare alle origini. Può essere usato per impedire a un utente non amministratore di passare a una nuova origine durante un'installazione, una reinstallazione o una riparazione su richiesta di installazione. Se [AllowLockdownMedia](allowlockdownmedia.md) è impostato, l'utente non amministratore potrebbe comunque installare un'applicazione gestita dal supporto con etichetta corretta.

DisableBrowse impedisce l'esplorazione da parte dell'utente non amministratore di un nuovo percorso multimediale o di qualsiasi altro percorso di origine. Per informazioni dettagliate su come proteggere le origini multimediali delle applicazioni gestite, vedere [resilienza dell'origine](source-resiliency.md).

Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).

 

 



