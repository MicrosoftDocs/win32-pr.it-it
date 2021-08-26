---
description: Introduzione allo sviluppo DirectShow filtro
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introduzione allo sviluppo DirectShow filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083691"
---
# <a name="introduction-to-directshow-filter-development"></a>Introduzione allo sviluppo DirectShow filtro

In questa sezione viene fornita una breve descrizione delle attività necessarie per lo sviluppo di un filtro DirectShow personalizzato. Vengono inoltre forniti collegamenti ad argomenti che illustrano queste attività in modo più dettagliato. Prima di leggere questa sezione, leggere gli argomenti in [Informazioni](about-directshow.md)DirectShow , che descrivono l'architettura DirectShow generale.

**DirectShow Libreria di classi di base**

L DirectShow SDK include un set di classi C++ per la scrittura di filtri. Anche se non sono obbligatorie, queste classi sono il modo consigliato per scrivere un nuovo filtro. Per usare le classi di base, compilarle in una libreria statica e collegare il file lib al progetto, come descritto in Compilazione di DirectShow [filtri](building-directshow-filters.md).

La libreria di classi di base definisce una classe radice per i filtri, la [**classe CBaseFilter.**](cbasefilter.md) Diverse altre classi derivano **da CBaseFilter** e sono specializzate per particolari tipi di filtri. Ad esempio, la [**classe CTransformFilter**](ctransformfilter.md) è progettata per i filtri di trasformazione. Per creare un nuovo filtro, implementare una classe che eredita da una delle classi di filtro. Ad esempio, la dichiarazione di classe potrebbe essere la seguente:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Per altre informazioni sulle classi DirectShow di base, vedere gli argomenti seguenti:

-   [DirectShow Classi di base](directshow-base-classes.md)
-   [Creazione DirectShow filtri](building-directshow-filters.md)

**Creazione di pin**

Un filtro deve creare uno o più pin. Il numero di pin può essere corretto in fase di progettazione oppure il filtro può creare nuovi pin in base alle esigenze. I pin in genere derivano dalla [**classe CBasePin**](cbasepin.md) o da una classe che eredita **CBasePin**, ad esempio [**CBaseInputPin**](cbaseinputpin.md). I pin del filtro devono essere dichiarati come variabili membro nella classe di filtro. Alcune classi di filtro definiscono già i pin, ma se il filtro eredita direttamente da **CBaseFilter**, è necessario dichiarare i pin nella classe derivata.

**Negoziazione delle connessioni pin**

Quando Gestione filtri Graph tenta di connettere due filtri, i pin devono essere d'accordo su vari aspetti. In caso contrario, il tentativo di connessione ha esito negativo. In genere, i pin negoziano quanto segue:

-   Transport. Il trasporto è il meccanismo che i filtri useranno per spostare campioni multimediali dal pin di output al pin di input. Ad esempio, possono usare [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modello push") o l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modello pull").
-   Tipo di supporto. Quasi tutti i pin usano tipi di supporti per descrivere il formato dei dati che verranno recapitati.
-   Allocatore. L'allocatore è l'oggetto che crea i buffer che contengono i dati. I pin devono accettare quale pin fornirà l'allocatore. Devono anche concordare le dimensioni dei buffer, il numero di buffer da creare e altre proprietà del buffer.

Le classi di base implementano un framework per queste negoziazioni. È necessario completare i dettagli eseguendo l'override di vari metodi nella classe di base. Il set di metodi di cui è necessario eseguire l'override dipende dalla classe e dalla funzionalità del filtro. Per altre informazioni, vedere [How Filters Connessione](how-filters-connect.md).

**Elaborazione e distribuzione di dati**

La funzione principale della maggior parte dei filtri è elaborare e distribuire i dati multimediali. Il modo in cui si verifica dipende dal tipo di filtro:

-   Un'origine push ha un thread di lavoro che riempie continuamente gli esempi di dati e li recapita a valle.
-   Un'origine pull attende che il vicino downstream richiedi un esempio. Risponde scrivendo dati in un esempio e fornendo l'esempio al filtro downstream. Il filtro downstream crea il thread che guida il flusso di dati.
-   Un filtro di trasformazione contiene campioni recapitati dal relativo vicino a monte. Quando riceve un esempio, elabora i dati e lo recapita a valle.
-   Un filtro renderer riceve campioni da upstream e li pianifica per il rendering in base ai timestamp.

Altre attività correlate allo streaming includono lo scaricamento dei dati dal grafo, la gestione della fine del flusso e la risposta alle richieste di ricerca. Per altre informazioni su questi problemi, vedere gli argomenti seguenti:

-   [Dati Flow per sviluppatori di filtri](data-flow-for-filter-developers.md)
-   [Gestione del controllo di qualità](quality-control-management.md)
-   [Thread e sezioni critiche](threads-and-critical-sections.md)

**Supporto di COM**

DirectShow filtri sono oggetti COM, in genere in pacchetto nelle DLL. La libreria di classi di base implementa un framework per il supporto di COM. È descritto nella sezione DirectShow [e COM](directshow-and-com.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



