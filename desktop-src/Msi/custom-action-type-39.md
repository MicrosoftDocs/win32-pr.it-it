---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 39 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo di azione personalizzata 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882734"
---
# <a name="custom-action-type-39"></a>Tipo di azione personalizzata 39

Il tipo di azione personalizzata 39 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

Digitare 39 azione personalizzata consente di installare un'applicazione annunciata o già installata. Questo tipo di azione personalizzata può essere utilizzato per reinstallare o rimuovere un prodotto che è stato installato come installazione simultanea dal pacchetto di installazione del prodotto corrente. Non è possibile usare l'azione personalizzata di tipo 39 per reinstallare o rimuovere il prodotto precedentemente installato in qualsiasi altro modo. Se, ad esempio, il prodotto secondario viene installato utilizzando un tipo 39, un tipo 23 o un'azione personalizzata di tipo 7 durante l'installazione del prodotto principale, è possibile utilizzare un'azione personalizzata di tipo 39 per rimuovere il prodotto secondario quando viene disinstallato il prodotto primario.

## <a name="source"></a>Source (Sorgente)

Il campo di origine della [tabella CustomAction](customaction-table.md) contiene il codice prodotto per l'applicazione.

## <a name="numeric-type"></a>Tipo numerico



| Nome tipo                                                     | Valore |
|---------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory | 39    |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene le impostazioni delle proprietà che devono essere passate all'installazione simultanea. Queste impostazioni delle proprietà possono specificare funzionalità.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Il tipo di azione personalizzata 39 ha esito negativo se l'applicazione non è annunciata o installata. Per evitare questo errore, è necessario impostare **msidbCustomActionTypeContinueflag**.

Non è possibile eseguire un'installazione simultanea in modo asincrono.

Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Sono disponibili flag di opzioni che consentono di controllare la potenziale esecuzione multipla di azioni personalizzate. Vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

L'azione personalizzata non usa questa opzione.

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
</dt> </dl>

 

 



