---
description: Accesso al catalogo COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Accesso al catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305025"
---
# <a name="accessing-the-com-catalog"></a>Accesso al catalogo COM+

Il catalogo COM+ è l'archivio dati sottostante che include tutti i dati di configurazione COM+. Ogni volta che si esegue qualsiasi tipo di amministrazione COM+, si leggono e si scrivono i dati archiviati nel catalogo. L'unico modo per accedere al catalogo è tramite lo strumento di amministrazione Servizi componenti o tramite la libreria COMAdmin.

Il catalogo COM+ fornisce un livello di astrazione rispetto ai dettagli effettivi sulla posizione e sulla modalità di archiviazione dei dati di configurazione COM+. Gran parte dei dati viene archiviata nel database di registrazione COM+ (o RegDB), che include i dati per tutti i componenti configurati installati nelle applicazioni COM+. Questo database viene utilizzato in fase di esecuzione dell'applicazione per fornire i dati di configurazione a COM+ per attivare correttamente gli oggetti in un contesto appropriato, consentendo la fornitura di servizi per gli oggetti in base alla configurazione. RegDB è un gestore di risorse transazionale che usa transazioni DTC tramite [Gestione risorse di compensazione](com--compensating-resource-manager.md). Quando si eseguono modifiche di configurazione salvate in modo permanente, ne viene eseguito il commit in modo transazionale. L'unico modo per accedere a RegDB è tramite il catalogo COM+, usando gli oggetti COMAdmin o lo strumento di amministrazione Servizi componenti.

In ogni computer è presente un server di catalogo COM+ eseguito come componente nell'applicazione di sistema. Il server di catalogo controlla l'accesso ai dati del catalogo archiviati nel relativo computer; il server di catalogo è in effetti un motore di query che consente di leggere e scrivere dati nel catalogo di tale computer. Quando si avvia l'amministrazione a livello di codice creando un'istanza di un oggetto [**COMAdminCatalog**](comadmincatalog.md) , questo oggetto apre una sessione con il server di catalogo locale. Le richieste di raccolte o elementi della raccolta nel catalogo locale vengono gestite dal server di catalogo locale. Quando ci si connette a un computer remoto, si comunica con il server di catalogo nel computer.

## <a name="security-considerations-in-administration"></a>Considerazioni sulla sicurezza nell'amministrazione

Per modificare i dati nel catalogo COM+, è necessario disporre dell'autorità come amministratore. Per utilizzare lo strumento di amministrazione Servizi componenti per modificare i dati di configurazione, è necessario essere un membro del ruolo amministratore assegnato all'applicazione di sistema nel computer che si sta tentando di amministrare. Analogamente, per modificare i dati utilizzando gli oggetti COMAdmin, il codice deve essere eseguito con l'autorità di amministrazione. Ovvero, un'applicazione o uno script che utilizza gli oggetti COMAdmin deve essere eseguito con un account utente assegnato al ruolo amministratore nell'applicazione di sistema nel computer che sta tentando di amministrare. L'applicazione può accedere e modificare le informazioni del catalogo solo nella misura in cui l'account con cui è in esecuzione dispone di tale autorità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descrizione riepilogativa delle classi COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



