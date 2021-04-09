---
title: Regole di progettazione dell'interfaccia
description: In questa sezione viene fornito un breve riepilogo delle regole e delle linee guida di progettazione dell'interfaccia.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1cde73527ac79a2e4442910e3053ed96748337
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118494"
---
# <a name="interface-design-rules"></a>Regole di progettazione dell'interfaccia

In questa sezione viene fornito un breve riepilogo delle regole e delle linee guida di progettazione dell'interfaccia. Alcune di queste regole sono specifiche dell'architettura COM, mentre altre sono restrizioni imposte dal linguaggio di progettazione dell'interfaccia MIDL. Per informazioni dettagliate sulla progettazione dell'interfaccia COM, vedere [anatomia di un file IDL](anatomy-of-an-idl-file.md).

Per definizione, un oggetto non è un oggetto COM a meno che non implementi l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) o un'interfaccia derivata da **IUnknown**. Inoltre, le regole seguenti si applicano a tutte le interfacce implementate in un oggetto COM:

-   Devono avere un identificatore di interfaccia univoco (IID).
-   Devono essere non modificabili. Una volta creati e pubblicati, nessuna parte della relativa definizione potrebbe cambiare.
-   Tutti i metodi di interfaccia devono restituire un valore **HRESULT** in modo che le parti del sistema che gestiscono l'elaborazione remota possano segnalare errori RPC.
-   Tutti i parametri di stringa nei metodi di interfaccia devono essere Unicode.
-   I tipi di dati devono essere utilizzabili in remoto. Se non è possibile convertire un tipo di dati in un tipo utilizzabile in remoto, sarà necessario creare routine di marshalling e di unmarshalling personalizzate. Inoltre, **LPVOID** o **void \*** non ha significato in un computer remoto. Se necessario, utilizzare un puntatore a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

> [!Note]  
> L'implementazione corrente di MIDL non gestisce l'overload di funzioni o l'ereditarietà multipla.

 

## <a name="other-interface-design-considerations"></a>Altre considerazioni sulla progettazione dell'interfaccia

Utilizzare i puntatori ai dati con molta attenzione. Per ricreare i dati nello spazio degli indirizzi del processo chiamato, è necessario che il tempo di esecuzione RPC conosca le dimensioni esatte dei dati. Se, ad esempio, un **parametro \* char** punta a un buffer di caratteri anziché a un singolo carattere, non sarà possibile ricreare correttamente i dati. Usare la sintassi disponibile con MIDL per descrivere accuratamente le strutture dei dati rappresentate dalle definizioni del tipo.

L'inizializzazione è essenziale per i puntatori incorporati in matrici e strutture e passati attraverso i limiti dei processi. I puntatori non inizializzati possono funzionare quando vengono passati a un programma nello stesso spazio di processo, ma i proxy e gli stub presuppongono che tutti i puntatori siano inizializzati con indirizzi validi o siano null.

Prestare attenzione quando si esegue l'aliasing dei puntatori (permettendo ai puntatori di puntare alla stessa porzione di memoria). Se l'aliasing è intenzionale, questi puntatori devono essere dichiarati con alias nel file IDL. I puntatori dichiarati come non con alias non devono mai essere alias reciprocamente.

Prestare attenzione a come allocare e liberare memoria. Tenere presente che, a meno che non si specifichi in modo esplicito un oggetto COM (usando l'attributo [**allocate**](/windows/desktop/Midl/allocate) ) per non liberare una struttura di dati creata durante una chiamata out-of-process, la struttura verrà distrutta al completamento della chiamata. Si consideri inoltre il sovraccarico potenzialmente distruttivo creato dall'allocazione inefficiente di strutture di dati di cui è ora necessario effettuare il marshalling e l'unmarshalling.

Infine, prestare attenzione quando si definiscono i valori restituiti **HRESULT** in modo da non creare codici di errore in conflitto con i codici ITF della funzionalità definita da com \_ (i valori compresi tra 0x0000 e 0x01ff sono riservati) o in conflitto con altri valori **HRESULT** con lo stesso valore. Quando possibile, utilizzare i valori restituiti Universal COM Success e Failure e utilizzare un parametro [**out**](/windows/desktop/Midl/out-idl) , anziché un **HRESULT**, per restituire informazioni specifiche della chiamata di funzione.

Per altre informazioni, vedere i seguenti argomenti:

-   [Progettazione di interfacce utilizzabili in remoto](designing-remotable-interfaces.md)
-   [Uso di un'interfaccia COM](using-a-com-interface.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 