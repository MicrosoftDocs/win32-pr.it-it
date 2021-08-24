---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034;1&0034;, consente agli utenti non amministratori di installare applicazioni gestite da origini archiviate su supporti, ad esempio un \# CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8e280fbd4941c43221d2178811fe341d4f963657bc4e6e5c9e8a19ec31acf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821861"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

L'impostazione del valore [](system-policy.md) di questo criterio di sistema per computer su "1" consente agli utenti non amministratori di installare applicazioni gestite da origini archiviate su supporti, ad esempio un CD-ROM. [](m-gly.md) Vedere [Resilienza di origine.](source-resiliency.md) Ad esempio, se questo criterio è impostato, un utente non amministrativo può usare un'origine supporto per installare applicazioni assegnate o pubblicate o applicazioni installate per tutti gli utenti. L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.

Il valore predefinito di questo criterio è 1 solo nei computer che eseguono Windows Vista e che non sono aggiunti a un dominio. L'impostazione predefinita in altri computer è che gli utenti non amministratori non possono installare applicazioni gestite da un'origine che si trova nei supporti.

Poiché questo criterio consente agli utenti che non sono amministratori di installare con privilegi non disponibili per impostazione predefinita, prima di impostare questo criterio è necessario valutare se fornisce un livello di sicurezza appropriato per l'utente. L'impostazione predefinita è consigliata per garantire un ambiente sicuro.

Per altre informazioni sulla protezione delle installazioni e sull'uso dei certificati [digitali,](guidelines-for-authoring-secure-installations.md) vedere Linee guida per la creazione di installazioni protette e firme digitali e programma di installazione di [Windows](digital-signatures-and-windows-installer.md) e Download di un'installazione [da Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto del programma di installazione di Windows che installa o avvia tali programmi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



