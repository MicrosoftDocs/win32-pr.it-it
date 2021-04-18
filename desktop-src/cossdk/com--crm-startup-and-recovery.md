---
description: Avvio e ripristino di COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Avvio e ripristino di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305232"
---
# <a name="com-crm-startup-and-recovery"></a>Avvio e ripristino di COM+ CRM

Se per un'applicazione server è selezionata la casella di controllo **Abilita gestori delle risorse di compensazione** (utilizzando lo strumento di amministrazione Servizi componenti, nella scheda **Avanzate** della pagina delle proprietà dell'applicazione com+), alla prima avvio viene creato un file di log CRM che verrà utilizzato da tutti dispongono nel processo dell'applicazione server. Per istruzioni dettagliate sulla configurazione del CRM, vedere [Configuring com+ CRM Components](configuring-com--crm-components.md).

Il nome del file di log CRM creato per l'applicazione server è basato sull'AppId (un GUID) dell'applicazione server e il file di log CRM si trova nella stessa directory del file di log DTC (in genere la directory% SystemRoot% \\ WinNT \\ system32 \\ DtcLog). I file di log CRM hanno estensione. crmlog.

> [!Note]  
> Potrebbe essere necessario modificare il percorso predefinito di un file di log CRM a causa delle prestazioni (in modo che il file di log DTC si trovi in un disco diverso rispetto al file di log CRM) o forse a causa dell'uso del CRM in un ambiente cluster. Il percorso dei file di log CRM può essere modificato utilizzando COM+ Administration SDK. Il nome della proprietà è CRMLogFile e esiste nell'oggetto raccolta [**Applications**](applications.md) .

 

Quando un'applicazione server (abilitata per CRM) viene avviata e rileva che un file di log CRM esiste già per quell'applicazione server, esegue il ripristino sul file di log CRM. Il *ripristino* è il processo di completamento di tutte le transazioni interrotte da un errore e prevede che l'infrastruttura CRM legga il file di log CRM per tutte le transazioni che non sono state completate correttamente. Se trova, contatta il DTC per determinare il risultato della transazione. Crea quindi il compensatore CRM e passa le notifiche commit o Interrompi come richiesto, insieme ai record di log associati.

Le notifiche di preparazione non vengono ricevute dal compensatore CRM durante il ripristino. Il compensatore CRM dispone di un flag per distinguere se viene chiamato durante il normale funzionamento o durante il ripristino.

Il ripristino rileverà normalmente le transazioni non completate solo se l'applicazione server è stata arrestata in modo anomalo a causa di un arresto anomalo del processo dell'applicazione server o di un arresto anomalo del computer. Se l'applicazione server può essere arrestata normalmente, a causa del timeout di inattività o dell'arresto manuale tramite lo strumento di amministrazione Servizi componenti, il file di log verrà pulito.

L'avvio di un'applicazione server CRM per il ripristino non viene avviato automaticamente. È necessario intraprendere un'azione esterna per avviare l'applicazione server CRM in cui è necessario il ripristino. In genere si creerebbe un componente in tale applicazione server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Processo operativo COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



