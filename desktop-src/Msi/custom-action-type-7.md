---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 7 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo di azione personalizzata 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050153"
---
# <a name="custom-action-type-7"></a>Tipo di azione personalizzata 7

Il tipo di azione personalizzata 7 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per ulteriori informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

Questa azione personalizzata consente di installare un altro pacchetto di installazione annidato all'interno del primo pacchetto.

## <a name="source"></a>Source (Sorgente)

Il database dell'applicazione simultanea viene archiviato come sottoarchivio del pacchetto e il nome della sottoarchiviazione viene designato nel campo di origine della [tabella CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numerico



| Nome tipo                                                      | Valore |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene le impostazioni delle proprietà da passare all'installazione simultanea. Queste impostazioni delle proprietà possono specificare funzionalità.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

La sessione di installazione simultanea viene eseguita come thread separato nel processo corrente. Un'installazione simultanea non può essere eseguita in modo asincrono.

Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Sono disponibili flag di opzioni che consentono di controllare la potenziale esecuzione multipla di azioni personalizzate. Vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Questa azione personalizzata non usa questa opzione.

## <a name="return-values"></a>Valori restituiti

Lo stato di restituzione dell'uscita utente, dell'esito negativo, della sospensione o dell'esito positivo di un'installazione simultanea viene elaborato nello stesso modo di qualsiasi altra azione. Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success. Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).

Si noti che se l'installazione simultanea è impostata su **msidbCustomActionTypeContinue** , viene restituito l'errore install \_ \_ USEREXIT, Error Install reboot \_ \_ , ERROR \_ install \_ reboot \_ Now oppure Error \_ Success \_ reboot \_ Required viene considerato come errore \_ riuscito. Ciò significa che se si imposta **msidbCustomActionTypeContinue** e l'installazione simultanea richiede un riavvio, il requisito per il riavvio verrà ignorato. Inoltre, il codice di errore dell'azione personalizzata di installazione simultanea verrà ignorato.

Se **msidbCustomActionTypeContinue** non è impostato, i codici restituiti seguenti più l'errore \_ Success vengono considerati come operazione riuscita e hanno i significati seguenti. Altri codici restituiti vengono considerati come errori.



| Messaggio                          | Significato                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERRORE \_ installazione \_ riavvio           | Il flag di riavvio verrà impostato per il riavvio alla fine dell'installazione.                                  |
| ERRORE \_ installazione \_ riavvio \_ ora      | Per completare l'installazione, è necessario riavviare il. Il riavvio verrà elaborato immediatamente. |
| ERRORE \_ di \_ riavvio \_ necessario | È stato richiesto un riavvio, ma è stato eliminato.                                                          |



 

## <a name="remarks"></a>Commenti

Un'espressione condizionale è necessaria per abilitare l'installazione simultanea durante l'installazione o la rimozione del componente o della funzionalità associata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazioni simultanee](concurrent-installations.md)
</dt> <dt>

[Riferimento all'azione personalizzata](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> <dt>

[Valori restituiti dell'azione personalizzata](custom-action-return-values.md)
</dt> </dl>

 

 



