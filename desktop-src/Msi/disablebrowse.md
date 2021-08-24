---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034;1&0034; impedisce agli utenti non amministratori di usare una finestra di dialogo sfoglia per individuare le origini delle applicazioni gestite archiviate nei supporti, ad esempio \# CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e565cca833d8d771b5bc28dea4483049868995a06acc9a42116611a1df6ce098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745571"
---
# <a name="disablebrowse"></a>DisableBrowse

L'impostazione del valore [](system-policy.md) di questo criterio di sistema per computer su "1" impedisce [](m-gly.md) agli utenti non amministratori di usare una finestra di dialogo Sfoglia per individuare le origini delle applicazioni gestite archiviate su supporti, ad esempio CD-ROM. [](browse-dialog.md) La casella combinata "Usa funzionalità da:" per l'input diretto è bloccata e l'opzione "Sfoglia..." il pulsante è disabilitato. Per altri dettagli sull'esplorazione dell'origine, vedere [Resilienza dell'origine.](source-resiliency.md)

DisableBrowse esegue l'override di AllowLockdownBrowse e impedisce l'esplorazione anche se AllowLockdownBrowse è impostato.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del computer** \\  \\ **locale** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

In alcuni casi con l'impostazione DisableBrowse, un utente non amministrativo potrebbe comunque essere in grado di installare applicazioni gestite da origini su supporti etichettati correttamente. L'impostazione del criterio DisableBrowse disabilita solo la funzionalità di esplorazione delle origini. Può essere usato per impedire a un utente non amministratore di accedere a una nuova origine durante un'installazione, una reinstallazione o un ripristino su richiesta. Se [l'opzione AllowLockdownMedia](allowlockdownmedia.md) è impostata, l'utente non amministratore potrebbe comunque installare un'applicazione gestita da supporti etichettati correttamente.

DisableBrowse impedisce all'utente non amministratore di accedere a un nuovo percorso multimediale o a qualsiasi altro percorso di origine. Per informazioni dettagliate su come proteggere le origini multimediali delle applicazioni gestite, vedere [Resilienza dell'origine.](source-resiliency.md)

Per informazioni sull'interazione di questo criterio con le origini di installazione, vedere [Gestione delle origini di installazione](managing-installation-sources.md).

 

 



