---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 23 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Tipo di azione personalizzata 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885854"
---
# <a name="custom-action-type-23"></a>Tipo di azione personalizzata 23

Il tipo di azione personalizzato 23 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

Questa azione personalizzata consente di installare un altro pacchetto di installazione che risiede nell'albero di origine dell'applicazione.

## <a name="source"></a>Source (Sorgente)

Il percorso del pacchetto di installazione simultaneo viene specificato in relazione alla radice del percorso di origine visualizzato nel campo di origine della [tabella CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numerico



| Nome tipo                                                      | Valore |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile | 23    |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene le impostazioni delle proprietà che devono essere passate all'installazione simultanea. Queste impostazioni delle proprietà possono specificare funzionalità.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

La sessione di installazione simultanea viene eseguita come thread separato nel processo corrente. Un'installazione simultanea non può essere eseguita in modo asincrono.

Per altre informazioni, vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Sono disponibili flag di opzioni che consentono di controllare la potenziale esecuzione multipla di azioni personalizzate. Per altre informazioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Non usato.

## <a name="return-values"></a>Valori restituiti

Lo stato di restituzione dell'uscita utente, dell'esito negativo, della sospensione o dell'esito positivo di un'installazione simultanea viene elaborato nello stesso modo di qualsiasi altra azione. Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success. Per altre informazioni, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).

Si noti che se l'installazione simultanea è impostata su **msidbCustomActionTypeContinue** , viene restituito un errore di installazione di USEREXIT, il riavvio dell'installazione dell'errore, l'installazione del riavvio del sistema \_ \_ \_ \_ \_ \_ \_ ora o l'errore \_ \_ \_ di riavvio richiesto viene considerato come \_ esito positivo dell'errore. Ciò significa che se si imposta **msidbCustomActionTypeContinue** e l'installazione simultanea richiede un riavvio, il requisito per il riavvio verrà ignorato. Inoltre, il codice di errore dell'azione personalizzata di installazione simultanea verrà ignorato.

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

 

 



