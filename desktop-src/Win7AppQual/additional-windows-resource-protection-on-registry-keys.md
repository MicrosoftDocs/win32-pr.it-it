---
description: Protezione Windows risorse aggiuntive nelle chiavi del Registro di sistema
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protezione Windows risorse aggiuntive nelle chiavi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ea823b2075905b8f22cbc02539f058c9ad8f2ed33ed51d712cd8cb43f59d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995021"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Protezione Windows risorse aggiuntive nelle chiavi del Registro di sistema

## <a name="platform"></a>Piattaforma

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Bassa  


## <a name="description"></a>Descrizione

Altre risorse di sistema hanno aggiunto Windows impostazioni WRP (Resource Protection) in Windows 7, rendendole impostazioni di sola lettura. La maggior parte delle risorse che hanno ricevuto una protezione aggiunta sono chiavi del server COM di sistema, anche se alcune funzionalità hanno aggiunto la protezione delle risorse di destinazione. Microsoft ha modificato queste risorse per proteggere il sistema e altre applicazioni dall'interruzione reciproca e per fornire una piattaforma coerente e stabile su cui le applicazioni possono essere eseguite in modo affidabile. In passato, le applicazioni potevano fornire file personalizzati e usare la registrazione COM non protetta per modificare il sistema. Nel caso di applicazioni meno recenti, questo può eseguire il downgrade dei runtime di sistema o modificare l'interfaccia su cui altre applicazioni dovevano funzionare correttamente. Nel peggiore dei casi, tali installazioni potrebbero causare errori di sistema o degradazione nel tempo. Per offrire un'esperienza migliore e una piattaforma di applicazioni più stabile, queste registrazioni sono bloccate in modo che solo gli aggiornamenti Microsoft potrebbero modificare i componenti di sistema.

Poiché la maggior parte delle risorse modificate sono chiavi COM usate dal sistema, questa modifica non influirà sulla maggior parte delle applicazioni. Sebbene la maggior parte delle applicazioni abbia un'esperienza migliore Windows 7 come risultato di queste modifiche, un piccolo subset di applicazioni potrebbe essere influenzato negativamente. I livelli di compatibilità delle applicazioni del sistema risolveranno automaticamente i problemi di installazione indicando sempre all'applicazione che è riuscita a modificare un'impostazione, anche se non è riuscita a causa di una risorsa protetta. Ciò impedisce l'interruzione delle impostazioni dell'applicazione, ma può causare problemi se è necessario modificare l'impostazione per il corretto funzionamento dell'applicazione.

## <a name="manifestation"></a>Manifestazione

Le applicazioni potrebbero aver modificato queste impostazioni prima di Windows 7. Dopo l'installazione in Windows 7, è possibile che alcune funzionalità non funzionino più perché le impostazioni non rispecchiano le previsioni dell'applicazione.

Esistono due scenari in cui le applicazioni possono riscontrare problemi correlati a questa protezione aggiunta:

-   Applicazioni che potrebbero aver utilizzato le impostazioni ora protette come archivio dati o come punto di estendibilità raro o non intenzionale
-   In rari casi, il meccanismo di rilevamento usato per identificare le configurazioni dell'applicazione potrebbe non riconoscere una configurazione specifica e quindi il livello di mitigazione della compatibilità delle applicazioni potrebbe non essere applicato

## <a name="mitigation"></a>Strategia di riduzione del rischio

Il principale mezzo di mitigazione è il livello di compatibilità delle applicazioni del sistema, che viene applicato automaticamente alle configurazioni delle applicazioni quando vengono rilevate. È anche possibile applicarlo manualmente a qualsiasi applicazione usando la scheda di compatibilità nelle proprietà dell'applicazione.

Questo livello risolve il problema intercettando le operazioni del Registro di sistema. Nel caso in cui l'applicazione tentava di modificare un'impostazione WRP (Read-Only), il livello restituisce sempre l'esito positivo, anche se l'impostazione non è stata effettivamente modificata. Per la maggior parte delle applicazioni, questo non causerà problemi. Esiste tuttavia la possibilità che l'applicazione sia stata modificata per il corretto funzionamento dell'impostazione, che è il primo scenario descritto in precedenza.

## <a name="solution"></a>Soluzione

Per i due scenari identificati in precedenza:

-   Se l'applicazione richiede che la chiave sia scrivibile per funzionare o usare l'archivio dati, non esiste altra soluzione se non modificare l'applicazione in modo che non esere più scrive in tale percorso.
-   Se il livello di compatibilità non è stato applicato a un'installazione, l'errore di installazione deve essere rilevato e offerto per l'applicazione e la rieseguiti. Le applicazioni possono anche essere eseguite in modalità di compatibilità, nel qual caso il livello di mitigazione viene sempre applicato.

## <a name="compatibility-tests"></a>Test di compatibilità

Come rilevare se a un'applicazione è stata applicata la mitigazione WRP:

-   Windows Il programma di installazione è a conoscenza di WRP; ignora automaticamente e invisibile all'utente i tentativi di scrittura o modifica di una risorsa protetta. Se l'applicazione è stata installata con Windows Installer ed è stata abilitata la registrazione, verrà registrato un avviso per ogni operazione di scrittura della chiave del Registro di sistema ignorata perché è una risorsa protetta da WRP.
-   L'API WRP incorpora SfCIsKeyProtected, che può eseguire query se una chiave del Registro di sistema è protetta da WRP nel sistema corrente. Per altre informazioni sull'uso di questa API, vedere la voce WRP in MSDN nei collegamenti seguenti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Windows Protezione delle risorse](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
