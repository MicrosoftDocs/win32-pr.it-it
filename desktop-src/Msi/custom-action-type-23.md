---
description: Gli sviluppatori di Windows Installer possono scegliere di usare un'azione personalizzata di tipo 23 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Tipo di azione personalizzata 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eeeb7e1056b9644baecdc8a4e5da959ad7320c960ea1de2ad38f9868f6e4c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637876"
---
# <a name="custom-action-type-23"></a>Tipo di azione personalizzata 23

Il tipo di azione personalizzata 23 viene usato con installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [Installazioni simultanee.](concurrent-installations.md)

Questa azione personalizzata installa un altro pacchetto del programma di installazione che risiede nell'albero di origine dell'applicazione.

## <a name="source"></a>Source (Sorgente)

Il percorso del pacchetto di installazione simultanea viene specificato in relazione alla radice del percorso di origine indicato nel campo Origine della [tabella CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numerico



| Nome tipo                                                      | Valore |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile | 23    |



 

## <a name="target"></a>Destinazione

Il campo Target della [tabella CustomAction contiene](customaction-table.md) le impostazioni delle proprietà che devono essere passate all'installazione simultanea. Queste impostazioni delle proprietà possono specificare funzionalità.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

La sessione di installazione simultanea viene eseguita come thread separato nel processo corrente. Un'installazione simultanea non può essere eseguita in modo asincrono.

Per altre informazioni, vedere [Custom Action Return Processing Options.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Sono disponibili flag di opzioni per controllare la potenziale esecuzione multipla di azioni personalizzate. Per altre informazioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Non usato.

## <a name="return-values"></a>Valori restituiti

Lo stato restituito di uscita dall'utente, errore, sospensione o esito positivo da un'installazione simultanea viene elaborato come qualsiasi altra azione. Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Ad esempio, se il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito ERROR \_ SUCCESS. Per altre informazioni, vedere [Registrazione dei valori restituiti dell'azione.](logging-of-action-return-values.md)

Si noti che se per un'installazione simultanea è impostato **msidbCustomActionTypeContinue,** la restituzione di ERROR \_ INSTALL \_ USEREXIT, ERROR INSTALL REBOOT, ERROR INSTALL REBOOT NOW o ERROR SUCCESS REBOOT REQUIRED viene considerata come \_ \_ ERROR \_ \_ \_ \_ \_ \_ \_ SUCCESS. Ciò significa che se si imposta **msidbCustomActionTypeContinue** e l'installazione simultanea richiede un riavvio, il requisito per il riavvio verrà ignorato. Inoltre, il codice di errore dell'azione personalizzata di installazione simultanea verrà ignorato.

Se **msidbCustomActionTypeContinue** non è impostato, i codici restituiti seguenti più ERROR SUCCESS vengono considerati con esito positivo e \_ hanno i significati seguenti. Altri codici restituiti vengono considerati come errori.



| Messaggio                          | Significato                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERRORE DURANTE \_ L'INSTALLAZIONE \_ DEL RIAVVIO           | Il flag di riavvio verrà impostato per il riavvio al termine dell'installazione.                                  |
| ERRORE DURANTE \_ L'INSTALLAZIONE \_ \_ RIAVVIO ORA      | Prima di completare l'installazione, è necessario riavviare il computer. Il riavvio verrà elaborato immediatamente. |
| ERRORE ESITO \_ POSITIVO \_ RIAVVIO \_ NECESSARIO | È stato richiesto un riavvio, ma è stato eliminato.                                                          |



 

## <a name="remarks"></a>Commenti

È necessaria un'espressione condizionale per abilitare l'installazione simultanea in fase di installazione o rimozione del componente o della funzionalità associata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazioni simultanee](concurrent-installations.md)
</dt> <dt>

[Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> <dt>

[Valori restituiti dell'azione personalizzata](custom-action-return-values.md)
</dt> </dl>

 

 



