---
description: Avvio e ripristino di COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Avvio e ripristino di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f65b8b1e32f2b587f7c288c6c5147ef30148360e89fc0a04ac952c8630076e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129193"
---
# <a name="com-crm-startup-and-recovery"></a>Avvio e ripristino di COM+ CRM

Se per un'applicazione server è selezionata la casella di controllo Abilita  gestori risorse di compensazione (tramite lo strumento di amministrazione Servizi componenti, nella scheda Avanzate della pagina delle proprietà dell'applicazione COM+), al primo avvio viene creato un file di log CRM che verrà usato da tutti i CPM nel processo dell'applicazione server.  Per istruzioni dettagliate sulla configurazione di CRM, vedere [Configurazione dei componenti CRM COM+.](configuring-com--crm-components.md)

Il nome del file di log CRM creato per l'applicazione server è basato sull'AppId (un GUID) dell'applicazione server e il file di log CRM viene inserito nella stessa directory del file di log DTC (in genere la directory %SystemRoot% \\ winnt \\ system32 \\ DtcLog). I file di log crm hanno l'estensione crmlog.

> [!Note]  
> Potrebbe essere necessario modificare il percorso predefinito di un file di log CRM per motivi di prestazioni (per avere il file di log DTC su un disco diverso da quello del file di log CRM) o forse a causa dell'uso di CRM in un ambiente cluster. Il percorso dei file di log crm può essere modificato usando l'SDK di amministrazione COM+. Il nome della proprietà è CRMLogFile ed è presente [**nell'oggetto raccolta**](applications.md) Applications.

 

Quando un'applicazione server abilitata per CRM viene avviata e rileva che esiste già un file di log CRM per tale applicazione server, esegue il ripristino su tale file di log CRM. *Il* ripristino è il processo di completamento di tutte le transazioni interrotte da un errore e comporta la lettura del file di log CRM da parte dell'infrastruttura CRM per tutte le transazioni non completate. Se ne trova uno, contatta DTC per determinare il risultato della transazione. Crea quindi crm Compensator e passa le notifiche di commit o interruzione in base alle esigenze, insieme ai record di log associati.

Le notifiche di preparazione non vengono ricevute da CRM Compensator durante il ripristino. CRM Compensator ha un flag per distinguere se viene chiamato durante il normale funzionamento o durante il ripristino.

Il ripristino in genere troverà transazioni non completate solo se l'applicazione server è stata arrestata in modo anomalo, a causa di un arresto anomalo del processo dell'applicazione server o di un arresto anomalo del computer. Se l'applicazione server può essere arrestata normalmente, a causa del timeout di inattività o dell'arresto manuale tramite lo strumento di amministrazione Servizi componenti, il file di log sarà pulito.

L'avvio di un'applicazione server CRM per il ripristino non viene avviato automaticamente. È necessario eseguire alcune azioni esterne per avviare l'applicazione server CRM in cui è necessario il ripristino. In genere si tratta della creazione di un componente in tale applicazione server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Processo operativo CRM COM+](com--crm-operating-process.md)
</dt> </dl>

 

 



