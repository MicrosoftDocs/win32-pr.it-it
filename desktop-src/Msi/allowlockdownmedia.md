---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; consente agli utenti non amministratori di installare applicazioni gestite da origini archiviate in supporti, ad esempio un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886030"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

L'impostazione del valore di questo criterio di [sistema](system-policy.md) per computer su "1" consente agli utenti non amministratori di installare [*applicazioni gestite*](m-gly.md) da origini archiviate su supporti, ad esempio un CD-ROM. Vedere [resilienza del codice sorgente](source-resiliency.md). Se, ad esempio, questo criterio è impostato, un utente non amministratore può utilizzare un'origine multimediale per installare le applicazioni assegnate o pubblicate o installate per tutti gli utenti. L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.

Il valore predefinito di questo criterio è 1 solo nei computer che eseguono Windows Vista e che non sono aggiunti a un dominio. Il valore predefinito di altri computer è che gli utenti non amministratori non possono installare le applicazioni gestite da un'origine situata nei supporti.

Poiché questo criterio consente agli utenti che non sono amministratori di installare con privilegi che non dispongono per impostazione predefinita, prima di impostare questo criterio è necessario valutare se fornisce un livello di sicurezza appropriato per l'utente. L'impostazione predefinita è consigliata per garantire un ambiente protetto.

Per ulteriori informazioni sulla protezione delle installazioni e sull'utilizzo di certificati digitali, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) e [il download di un'installazione da Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto di Windows Installer per l'installazione o l'avvio di tali programmi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



