---
description: Accesso al catalogo COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Accesso al catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f05d85526cb6d82916aa48a49c7f97e581c01b7410530878a7f6e0fc69dac20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129413"
---
# <a name="accessing-the-com-catalog"></a>Accesso al catalogo COM+

Il catalogo COM+ è l'archivio dati sottostante che contiene tutti i dati di configurazione COM+. Ogni volta che si eseggono tipi di amministrazione COM+, si leggono e scrivono dati archiviati nel catalogo. L'unico modo per accedere al catalogo è tramite lo strumento amministrativo Servizi componenti o tramite la libreria COMAdmin.

Il catalogo COM+ fornisce un livello di astrazione sui dettagli effettivi della posizione e della modalità di archiviazione dei dati di configurazione COM+. Gran parte dei dati viene archiviata nel database di registrazione COM+ (o RegDB), che contiene i dati per tutti i componenti configurati installati nelle applicazioni COM+. Questo database viene usato in fase di esecuzione dell'applicazione per fornire dati di configurazione a COM+ per attivare correttamente gli oggetti in un contesto appropriato, consentendo di fornire servizi per gli oggetti in base alla configurazione. RegDB è un gestore di risorse transazionale che usa transazioni DTC tramite il [gestore delle risorse di compensazione.](com--compensating-resource-manager.md) Quando si apportano modifiche di configurazione persistenti, ne viene eseguito il commit in modo transazionale. L'unico modo per accedere a RegDB è tramite il catalogo COM+, usando gli oggetti COMAdmin o lo strumento amministrativo Servizi componenti.

In ogni computer è presente un server di catalogo COM+ in esecuzione come componente nell'applicazione di sistema. Il server di catalogo controlla l'accesso ai dati del catalogo archiviati nel computer; in effetti, il server di catalogo è un motore di query che consente di leggere e scrivere dati nel catalogo in tale computer. Quando si avvia l'amministrazione a livello di codice creando un'istanza di un [**oggetto COMAdminCatalog,**](comadmincatalog.md) questo oggetto apre una sessione con il server di catalogo locale. Le richieste di raccolte o elementi di raccolta nel catalogo locale vengono gestite dal server di catalogo locale. Quando ci si connette a un computer remoto, si comunica con il server di catalogo in tale computer.

## <a name="security-considerations-in-administration"></a>Considerazioni sulla sicurezza nell'amministrazione

Per modificare i dati nel catalogo COM+, è necessario avere l'autorità di amministratore. Per usare lo strumento amministrativo Servizi componenti per modificare i dati di configurazione, è necessario essere un membro del ruolo Administrators assegnato all'applicazione di sistema nel computer che si sta tentando di amministrare. Analogamente, per modificare i dati usando gli oggetti COMAdmin, il codice deve essere eseguito con l'autorità di amministrazione. Ciò significa che un'applicazione o uno script che usa gli oggetti COMAdmin deve essere in esecuzione con un account utente assegnato al ruolo Administrators nell'applicazione di sistema nel computer che sta tentando di amministrare. L'applicazione può accedere e modificare le informazioni nel catalogo solo nella misura in cui l'account con cui è in esecuzione dispone di tale autorità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descrizione di riepilogo delle classi COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



