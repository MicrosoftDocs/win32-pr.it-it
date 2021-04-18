---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protezione risorse di Windows aggiuntive sulle chiavi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318898"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Protezione risorse di Windows aggiuntive sulle chiavi del registro di sistema

## <a name="platform"></a>Piattaforma

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -bassa  


## <a name="description"></a>Descrizione

Altre risorse di sistema hanno aggiunto le impostazioni Protezione risorse di Windows (WRP) in Windows 7, rendendole impostazioni di sola lettura. La maggior parte delle risorse che hanno ricevuto una protezione aggiuntiva è costituita da chiavi server COM di sistema, anche se alcune funzionalità hanno aggiunto la protezione delle risorse di destinazione. Microsoft ha modificato queste risorse per proteggere il sistema e le altre applicazioni e fornire una piattaforma stabile e coerente su cui possano essere eseguite in modo affidabile le applicazioni. In passato, le applicazioni potevano fornire file personalizzati e utilizzare la registrazione COM non protetta per modificare il sistema. Nel caso di applicazioni meno recenti, questo può effettuare il downgrade dei runtime di sistema o modificare l'interfaccia su cui altre applicazioni necessitano di funzionare correttamente. Nel peggiore dei casi, tali installazioni potrebbero causare un errore o un calo del sistema nel tempo. Per offrire un'esperienza migliore e una piattaforma applicativa più stabile, abbiamo bloccato queste registrazioni, in modo che solo gli aggiornamenti Microsoft potessero modificare i componenti di sistema.

Poiché la maggior parte delle risorse modificate sono chiavi COM utilizzate dal sistema, questa modifica non influirà sulla maggior parte delle applicazioni. Sebbene ci si aspetta che la maggior parte delle applicazioni abbia un'esperienza migliore in Windows 7 in seguito a queste modifiche, un piccolo subset di applicazioni potrebbe essere influenzato negativamente. I livelli di compatibilità delle applicazioni del sistema risolveranno automaticamente i problemi di installazione indicando sempre all'applicazione che è riuscita a modificare un'impostazione, anche se non è riuscita perché è una risorsa protetta. In questo modo si impedisce l'interruzioni delle configurazioni dell'applicazione, ma possono verificarsi problemi se è necessario modificare l'impostazione affinché l'applicazione funzioni correttamente.

## <a name="manifestation"></a>Manifestazione

Le applicazioni potrebbero avere modificato queste impostazioni prima di Windows 7. Quando si esegue l'installazione in Windows 7, le applicazioni potrebbero rilevare che alcune funzionalità non funzionano più perché le impostazioni non riflettono ciò che è previsto per l'applicazione.

Esistono due scenari in cui le applicazioni possono riscontrare problemi correlati a questa protezione aggiuntiva:

-   Applicazioni che potrebbero avere utilizzato le impostazioni protette da ora come archivio dati o come punto di estensibilità raro o non intenzionale
-   In rari casi, il meccanismo di rilevamento usato per identificare le configurazioni dell'applicazione potrebbe non riconoscere una particolare configurazione, quindi il livello di mitigazione della compatibilità delle applicazioni potrebbe non essere applicato

## <a name="mitigation"></a>Strategia di riduzione del rischio

Il metodo principale di mitigazione è il livello di compatibilità delle applicazioni del sistema, che viene applicato automaticamente alle configurazioni dell'applicazione quando viene rilevato. È anche possibile applicarla manualmente a qualsiasi applicazione usando la scheda compatibilità nelle proprietà dell'applicazione.

Questo livello risolve il problema intercettando le operazioni del registro di sistema. Nel caso in cui l'applicazione tenti di modificare un'impostazione di sola lettura (WRP), il livello restituisce sempre esito positivo, anche se l'impostazione non è stata effettivamente modificata. Per la maggior parte delle applicazioni, questa operazione non provocherà alcun problema. Tuttavia, è possibile che l'applicazione abbia richiesto l'impostazione modificata per funzionare correttamente, ovvero il primo scenario descritto in precedenza.

## <a name="solution"></a>Soluzione

Per i due scenari indicati in precedenza:

-   Se l'applicazione richiede che la chiave sia scrivibile per funzionare o usare l'archivio dati, non esiste alcuna soluzione diversa dalla modifica dell'applicazione in modo che non scriva più in tale posizione.
-   Se il livello di compatibilità non è stato applicato a una configurazione, l'errore di installazione deve essere rilevato e offerto per essere applicato ed eseguito nuovamente. Le applicazioni possono anche essere eseguite in modalità di compatibilità, nel qual caso il livello di mitigazione viene sempre applicato.

## <a name="compatibility-tests"></a>Test di compatibilità

Come rilevare se per un'applicazione è stata applicata la mitigazione WRP:

-   Windows Installer è a conoscenza di WRP; ignora automaticamente i tentativi di scrittura o modifica di una risorsa protetta. Se l'applicazione è stata installata con Windows Installer e la registrazione è stata abilitata, viene registrato un avviso per ogni operazione di scrittura della chiave del registro di sistema che è stata ignorata perché è una risorsa protetta da WRP.
-   L'API WRP incorpora SfCIsKeyProtected, che può eseguire una query se una chiave del registro di sistema è protetta da WRP nel sistema corrente. Per altre informazioni sull'uso di questa API, vedere la voce relativa a WRP in MSDN nei collegamenti seguenti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Protezione risorse di Windows](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
