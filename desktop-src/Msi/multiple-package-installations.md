---
description: Windows Il programma di installazione può installare più pacchetti usando l'elaborazione delle transazioni.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package installazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943412"
---
# <a name="multiple-package-installations"></a>Multiple-Package installazioni

Windows Il programma di installazione può installare più pacchetti usando [*l'elaborazione delle transazioni*](t-gly.md). Questa funzionalità è disponibile a partire da Windows Installer 4.5. Il programma di installazione installerà tutti i pacchetti appartenenti a una transazione con più pacchetti o nessuno dei pacchetti. Se tutti i pacchetti nella transazione non possono essere installati correttamente o se l'utente annulla l'installazione, il programma di installazione di Windows può eseguire il rollback delle modifiche e ripristinare lo stato originale del computer.

Un pacchetto di installazione a più pacchetti può contenere una tabella [MsiEmbeddedChainer](msiembeddedchainer-table.md) che fa riferimento a una funzione definita dall'utente che usa le funzioni [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)e [**MsiEndTransaction.**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)

La [tabella MsiPackageCertificate elenca](msipackagecertificate-table.md) i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che effettuano un'installazione con più pacchetti. È possibile usare questa tabella per ridurre il numero di volte in cui l'installazione di più pacchetti visualizza una richiesta di controllo [*dell'account*](u-gly.md) utente che richiede una risposta da parte di un amministratore.

Le funzioni Windows installer seguenti possono apportare modifiche al computer dell'utente quando il programma di installazione di Windows installa, ripristina, aggiorna o rimuove le applicazioni. A partire da Windows Installer 4.5, il programma di installazione [](t-gly.md) può eseguire il rollback delle modifiche apportate da queste funzioni durante l'elaborazione delle transazioni di un'installazione con più pacchetti:

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Esiste un'eccezione se Windows installer rileva un pacchetto appartenente a un'installazione a più pacchetti che contiene un'azione [ForceReboot](forcereboot-action.md) o [ScheduleReboot.](schedulereboot-action.md) In questo caso, Windows installer non installa solo il pacchetto. È possibile installare altri pacchetti che appartengono all'installazione a più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

**[Windows Installer 4.0](not-supported-in-windows-installer-4-0.md)e versioni precedenti:[****](t-gly.md) L'elaborazione delle transazioni di più pacchetti Windows di installazione non è supportata. Queste versioni del programma di Windows non sono in grado di eseguire il rollback dell'installazione di più pacchetti come singola transazione.

**Windows Server 2008 R2 [](../termserv/terminal-services-portal.md)** con il ruolo Servizi Desktop remoto abilitato: Non supportato. L'installazione di più pacchetti [tramite la tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) ha esito negativo [se il](../termserv/terminal-services-portal.md) Servizi Desktop remoto è abilitato.

 

 
