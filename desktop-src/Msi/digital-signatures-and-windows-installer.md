---
description: Il Windows Installer può usare le firme digitali per rilevare le risorse danneggiate.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Firme digitali e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315908"
---
# <a name="digital-signatures-and-windows-installer"></a>Firme digitali e Windows Installer

Il Windows Installer può usare le firme digitali per rilevare le risorse danneggiate. Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna da installare dal pacchetto. Per ulteriori informazioni sull'utilizzo di firme digitali, certificati digitali e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), vedere la sezione relativa alla [sicurezza](https://msdn.microsoft.com/library/cc527452.aspx) di Microsoft Windows Software Development Kit (SDK).

Con Windows Installer, le firme digitali possono essere utilizzate con Windows Installer pacchetti, trasformazioni, patch, moduli unione e file CAB esterni. Windows Installer è integrato con i criteri di restrizione software in Microsoft Windows XP. È possibile creare criteri per consentire o impedire installazioni basate su criteri diversi, ad esempio un certificato o un server di pubblicazione specifico. Il Windows Installer è in grado di eseguire la convalida della firma dei file CAB esterni su tutte le piattaforme in cui è installata la versione CryptoAPI 2,0.

Si noti che il bootstrap di esempio Setup.exe fornito con Windows Installer SDK esegue un controllo della firma su un pacchetto di Windows Installer prima di avviare l'installazione.

L'esecuzione di un' [installazione amministrativa](administrative-installation.md) rimuove la firma digitale dal pacchetto. Un'installazione amministrativa modifica il pacchetto di installazione per aggiungere il flusso AdminProperties, che invalida la firma digitale originale. Un amministratore può firmare nuovamente il pacchetto.

Se si applica una patch a un'installazione amministrativa, viene anche rimossa la firma digitale dal pacchetto. Il motivo è che le modifiche vengono mantenute nel pacchetto di installazione con patch dell'installazione amministrativa. Un amministratore può firmare nuovamente il pacchetto.

A partire da Windows Installer versione 3,0, l'applicazione di [patch al controllo dell'account utente](user-account-control--uac--patching.md) consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. L'applicazione di patch del controllo dell'account utente è abilitata fornendo un certificato di firma nella tabella [MsiPatchCertificate](msipatchcertificate-table.md) e firmando patch con lo stesso certificato.

Per ulteriori informazioni, vedere [firme digitali e file CAB esterni](digital-signatures-and-external-cabinet-files.md), [Windows Installer e criteri di restrizione software](windows-installer-and-software-restriction-policy.md), [creazione di un'installazione con firma completamente verificata](authoring-a-fully-verified-signed-installation.md)e [un URL basato Windows Installer esempio di installazione](a-url-based-windows-installer-installation-example.md).

 

 
