---
title: Regole di progettazione dell'interfaccia
description: Questa sezione fornisce un breve riepilogo delle linee guida e delle regole di progettazione dell'interfaccia.
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d11d55a1e24c02208ebeecddd5a4f90b8b01fa4a53444e6554cfcff37165f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070811"
---
# <a name="interface-design-rules"></a>Regole di progettazione dell'interfaccia

Questa sezione fornisce un breve riepilogo delle linee guida e delle regole di progettazione dell'interfaccia. Alcune di queste regole sono specifiche dell'architettura COM, mentre altre sono restrizioni imposte dal linguaggio di progettazione dell'interfaccia MIDL. Per informazioni dettagliate sulla progettazione dell'interfaccia COM, [vedere Anatomia di un file IDL.](anatomy-of-an-idl-file.md)

Per definizione, un oggetto non è un oggetto COM a meno che non implementi [**l'interfaccia IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) o un'interfaccia derivata da **IUnknown.** Inoltre, le regole seguenti si applicano a tutte le interfacce implementate in un oggetto COM:

-   Devono avere un identificatore di interfaccia (IID) univoco.
-   Devono essere non modificabili. Una volta creati e pubblicati, nessuna parte della relativa definizione può cambiare.
-   Tutti i metodi di interfaccia devono restituire **un valore HRESULT** in modo che le parti del sistema che gestiscono l'elaborazione remota possano segnalare errori RPC.
-   Tutti i parametri di stringa nei metodi di interfaccia devono essere Unicode.
-   I tipi di dati devono essere utilizzabili in remoto. Se non è possibile convertire un tipo di dati in un tipo utilizzabile in remoto, sarà necessario creare routine di marshalling e unmarshaling. Inoltre, **LPVOID** o **void \** _, non ha alcun significato in un computer remoto. Usare un puntatore [a _ *IUnknown* *](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), se necessario.

> [!Note]  
> L'implementazione corrente di MIDL non gestisce l'overload della funzione o l'ereditarietà multipla.

 

## <a name="other-interface-design-considerations"></a>Altre considerazioni sulla progettazione dell'interfaccia

Usare i puntatori ai dati con molta attenzione. Per creare nuovamente i dati nello spazio indirizzi del processo chiamato, il tempo di esecuzione RPC deve conoscere le dimensioni esatte dei dati. Se, ad esempio, un parametro **CHAR \*** punta a un buffer di caratteri anziché a un singolo carattere, i dati non possono essere ri-creati correttamente. Usare la sintassi disponibile con MIDL per descrivere in modo accurato le strutture dei dati rappresentate dalle definizioni dei tipi.

L'inizializzazione è essenziale per i puntatori incorporati in matrici e strutture e passati attraverso i limiti del processo. I puntatori non inizializzati possono funzionare quando vengono passati a un programma nello stesso spazio di processo, ma i proxy e gli stub presuppongono che tutti i puntatori siano inizializzati con indirizzi validi o siano Null.

Prestare attenzione quando si esegue l'aliasing dei puntatori ,consentendo ai puntatori di puntare alla stessa parte di memoria. Se l'aliasing è intenzionale, questi puntatori devono essere dichiarati come alias nel file IDL. I puntatori dichiarati come non alias non devono mai essere alias reciproci.

Prestare attenzione a come allocare e liberare memoria. Tenere presente che, se non si indica in modo esplicito a un oggetto COM (tramite l'attributo [**allocate)**](/windows/desktop/Midl/allocate) di non liberare una struttura di dati creata durante una chiamata out-of-process, tale struttura verrà distrutta al termine della chiamata. Considerare anche il sovraccarico potenzialmente distruttivo creato da un'allocazione inefficiente di strutture di dati che ora devono essere sottoposti a marshalling e di cui è necessario eseguire l'unmarsshaled.

Prestare infine attenzione quando si definiscono i valori **restituiti HRESULT** in modo da non creare codici di errore in conflitto con i codici ITF FACILITY definiti da COM (i valori compresi tra 0x0000 e 0x01FF sono riservati) o in conflitto con altri valori HRESULT con lo \_  stesso valore. Quando possibile, usare i valori restituiti universali com success e failure e usare un parametro [**out,**](/windows/desktop/Midl/out-idl) anziché **un HRESULT,** per restituire informazioni specifiche della chiamata di funzione.

Per altre informazioni, vedere i seguenti argomenti:

-   [Progettazione di interfacce remota](designing-remotable-interfaces.md)
-   [Uso di un'interfaccia COM](using-a-com-interface.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 