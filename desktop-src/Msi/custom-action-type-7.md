---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 7 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo di azione personalizzata 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6735546b4db55bc8f9875fa2cd267eb0877a52c92e0a0073a942165dc413055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947912"
---
# <a name="custom-action-type-7"></a>Tipo di azione personalizzata 7

Il tipo di azione personalizzata 7 viene usato con installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per altre informazioni sulle installazioni simultanee, vedere [Installazioni simultanee.](concurrent-installations.md)

Questa azione personalizzata installa un altro pacchetto del programma di installazione annidato all'interno del primo pacchetto.

## <a name="source"></a>Source (Sorgente)

Il database dell'applicazione simultanea viene archiviato come una sottostorage del pacchetto e il nome dell'archiviazione secondaria viene designato nel campo Source della [tabella CustomAction](customaction-table.md).

## <a name="numeric-type"></a>Tipo numerico



| Nome tipo                                                      | Valore |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>Destinazione

Il campo Target della tabella [CustomAction contiene](customaction-table.md) le impostazioni delle proprietà da passare all'installazione simultanea. Queste impostazioni delle proprietà possono specificare funzionalità.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

La sessione di installazione simultanea viene eseguita come thread separato nel processo corrente. Un'installazione simultanea non può essere eseguita in modo asincrono.

Vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Sono disponibili flag di opzioni per controllare la potenziale esecuzione multipla di azioni personalizzate. Vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Questa azione personalizzata non usa questa opzione.

## <a name="return-values"></a>Valori restituiti

Lo stato restituito di uscita dall'utente, errore, sospensione o esito positivo da un'installazione simultanea viene elaborato come qualsiasi altra azione. Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log. Ad esempio, se il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito ERROR \_ SUCCESS. Per altre informazioni su questa traduzione, vedere [Registrazione dei valori restituiti delle azioni.](logging-of-action-return-values.md)

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

 

 



