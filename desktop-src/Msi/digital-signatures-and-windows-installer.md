---
description: Il Windows installer può usare firme digitali per rilevare le risorse danneggiate.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Firme digitali e programma di Windows di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692811"
---
# <a name="digital-signatures-and-windows-installer"></a>Firme digitali e programma di Windows di installazione

Il Windows installer può usare firme digitali per rilevare le risorse danneggiate. Un certificato del firmatario può essere confrontato con il certificato del firmatario di una risorsa esterna che deve essere installato dal pacchetto. Per altre informazioni sull'uso di firme digitali, certificati digitali e [](https://msdn.microsoft.com/library/cc527452.aspx) [**WinVerifyTrust,**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)vedere la sezione Sicurezza di Microsoft Windows Software Development Kit (SDK).

Con Windows installer, le firme digitali possono essere usate con Windows, trasformazioni, patch, moduli unione e file cab esterni del programma di installazione. Windows Il programma di installazione è integrato con Criteri di restrizione software in Microsoft Windows XP. È possibile creare criteri per consentire o impedire le installazioni in base a criteri diversi, tra cui un certificato o un editore del firmatario specifico. Il Windows installer può eseguire la convalida della firma di file cab esterni in tutte le piattaforme in cui è installato CryptoAPI versione 2.0.

Si noti che l'esempio Setup.exe bootstrap fornito con Windows Installer SDK esegue un controllo della firma in un pacchetto di Windows Installer prima di avviare l'installazione.

[L'esecuzione di un'installazione](administrative-installation.md) amministrativa rimuove la firma digitale dal pacchetto. Un'installazione amministrativa modifica il pacchetto di installazione per aggiungere il flusso AdminProperties, che invaliderebbe la firma digitale originale. Un amministratore può dimettere il pacchetto.

L'applicazione di una patch a un'installazione amministrativa rimuove anche la firma digitale dal pacchetto. Il motivo è che le modifiche vengono mantenute nel pacchetto di installazione con patch dell'installazione amministrativa. Un amministratore può dimettere il pacchetto.

A partire da Windows Installer versione 3.0, l'applicazione di patch al controllo [dell'account](user-account-control--uac--patching.md) utente consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. L'applicazione di patch del controllo dell'account utente viene abilitata fornendo un certificato del firmatario nella tabella [MsiPatchCertificate](msipatchcertificate-table.md) e firmando le patch con lo stesso certificato.

Per altre informazioni, vedere Firme digitali e file CAB esterni [,](digital-signatures-and-external-cabinet-files.md)Programma di installazione [di Windows](windows-installer-and-software-restriction-policy.md)e Criteri di restrizione software [,](authoring-a-fully-verified-signed-installation.md)Creazione di un'installazione firmata completamente verificata e Esempio di installazione del programma di installazione di Windows basato su [URL](a-url-based-windows-installer-installation-example.md).

 

 
