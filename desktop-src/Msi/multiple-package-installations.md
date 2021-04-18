---
description: Windows Installer possibile installare più pacchetti utilizzando l'elaborazione delle transazioni.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Installazioni di Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310518"
---
# <a name="multiple-package-installations"></a>Installazioni di Multiple-Package

Windows Installer possibile installare più pacchetti utilizzando l' [*elaborazione delle transazioni*](t-gly.md). Questa funzionalità è disponibile a partire da Windows Installer 4,5. Il programma di installazione installerà tutti i pacchetti appartenenti a una transazione con più pacchetti o nessuno dei pacchetti. Se non è possibile installare tutti i pacchetti nella transazione o se l'utente annulla l'installazione, il Windows Installer possibile eseguire il rollback delle modifiche e ripristinare lo stato originale del computer.

Un pacchetto di installazione con più pacchetti può contenere una [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) che fa riferimento a una funzione definita dall'utente che usa le funzioni [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)e [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

La [tabella MsiPackageCertificate](msipackagecertificate-table.md) elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che effettuano l'installazione di più pacchetti. È possibile utilizzare questa tabella per ridurre il numero di volte in cui l'installazione di più pacchetti Visualizza un messaggio di [*controllo dell'account utente*](u-gly.md) (UAC) che richiede una risposta da parte di un amministratore.

Le seguenti funzioni di Windows Installer possono apportare modifiche al computer dell'utente quando il Windows Installer installa, Ripristina, aggiorna o rimuove le applicazioni. A partire da Windows Installer 4,5, il programma di installazione può eseguire il rollback delle modifiche apportate da queste funzioni durante l' [*elaborazione delle transazioni*](t-gly.md) di un'installazione con più pacchetti:

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

Si verifica un'eccezione se il Windows Installer rileva un pacchetto appartenente a un'installazione con più pacchetti che contiene un'azione [ForceReboot](forcereboot-action.md) o [ScheduleReboot](schedulereboot-action.md) . In questo caso, Windows Installer non installa solo quel pacchetto. È possibile installare altri pacchetti che appartengono all'installazione con più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md): * * l'[*elaborazione delle transazioni*](t-gly.md) di installazioni con più pacchetti Windows Installer non è supportata. Queste versioni del Windows Installer non sono in grado di eseguire il rollback dell'installazione di più pacchetti come una singola transazione.

**Windows Server 2008 R2 con il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato. L'installazione di più pacchetti con la [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) ha esito negativo se il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) è abilitato.

 

 
