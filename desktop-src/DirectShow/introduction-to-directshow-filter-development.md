---
description: Introduzione allo sviluppo di filtri DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introduzione allo sviluppo di filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303957"
---
# <a name="introduction-to-directshow-filter-development"></a>Introduzione allo sviluppo di filtri DirectShow

Questa sezione fornisce una breve descrizione delle attività necessarie per lo sviluppo di un filtro DirectShow personalizzato. Vengono inoltre forniti collegamenti ad argomenti che illustrano queste attività in modo più dettagliato. Prima di leggere questa sezione, leggere gli argomenti [relativi a DirectShow](about-directshow.md), che descrivono l'architettura complessiva di DirectShow.

**Libreria di classi base DirectShow**

DirectShow SDK include un set di classi C++ per la scrittura dei filtri. Sebbene non siano necessari, queste classi rappresentano la modalità consigliata per scrivere un nuovo filtro. Per usare le classi base, compilarle in una libreria statica e collegare il file con estensione LIB al progetto, come descritto in [creazione di filtri DirectShow](building-directshow-filters.md).

La libreria di classi di base definisce una classe radice per i filtri, la classe [**CBaseFilter**](cbasefilter.md) . Diverse altre classi derivano da **CBaseFilter** e sono specializzate per determinati tipi di filtri. Ad esempio, la classe [**CTransformFilter**](ctransformfilter.md) è progettata per i filtri di trasformazione. Per creare un nuovo filtro, implementare una classe che eredita da una delle classi di filtro. Ad esempio, la dichiarazione di classe potrebbe essere la seguente:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Per ulteriori informazioni sulle classi base di DirectShow, vedere gli argomenti seguenti:

-   [Classi base di DirectShow](directshow-base-classes.md)
-   [Creazione di filtri DirectShow](building-directshow-filters.md)

**Creazione di pin**

Un filtro deve creare uno o più pin. Il numero di pin può essere corretto in fase di progettazione oppure il filtro può creare nuovi PIN in base alle esigenze. I pin derivano in genere dalla classe [**CBasePin**](cbasepin.md) o da una classe che eredita **CBasePin**, ad esempio [**CBaseInputPin**](cbaseinputpin.md). I pin del filtro devono essere dichiarati come variabili membro nella classe filter. Alcune classi di filtro definiscono già i pin, ma se il filtro eredita direttamente da **CBaseFilter**, è necessario dichiarare i pin nella classe derivata.

**Negoziazione di connessioni pin**

Quando il gestore del grafico dei filtri tenta di connettere due filtri, i pin devono concordare su vari aspetti. In caso affermativo, il tentativo di connessione ha esito negativo. In genere, i pin negoziano quanto segue:

-   Transport. Il trasporto è il meccanismo che i filtri utilizzeranno per spostare gli esempi di supporti dal pin di output al pin di input. Ad esempio, è possibile usare l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modello push") o l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modello pull").
-   Tipo di supporto. Quasi tutti i pin utilizzano i tipi di supporto per descrivere il formato dei dati che verranno recapitati.
-   Allocatore. L'allocatore è l'oggetto che crea i buffer che contengono i dati. I pin devono accettare quale pin fornirà l'allocatore. Devono inoltre accettare le dimensioni dei buffer, il numero di buffer da creare e altre proprietà del buffer.

Le classi base implementano un Framework per queste negoziazioni. Per completare i dettagli, è necessario eseguire l'override di diversi metodi della classe di base. Il set di metodi di cui è necessario eseguire l'override dipende dalla classe e dalla funzionalità del filtro. Per ulteriori informazioni, vedere [la](how-filters-connect.md)pagina relativa alla modalità di connessione dei filtri.

**Elaborazione e distribuzione di dati**

La funzione principale della maggior parte dei filtri consiste nell'elaborare e distribuire i dati multimediali. Il modo in cui si verifica dipende dal tipo di filtro:

-   Un'origine push dispone di un thread di lavoro che compila continuamente campioni con dati e li recapita a valle.
-   Un'origine pull Attende che l'elemento adiacente downstream richieda un campione. Risponde scrivendo i dati in un esempio e recapitando l'esempio al filtro downstream. Il filtro downstream crea il thread che guida il flusso di dati.
-   A un filtro di trasformazione sono stati recapitati esempi dal rispettivo Neighbor upstream. Quando riceve un esempio, elabora i dati e li recapita a valle.
-   Un filtro renderer riceve esempi da upstream e li pianifica per il rendering in base agli indicatori temporali.

Altre attività correlate al flusso includono lo scaricamento dei dati dal grafico, la gestione della fine del flusso e la risposta alle richieste di ricerca. Per ulteriori informazioni su questi problemi, vedere gli argomenti seguenti:

-   [Flusso di dati per sviluppatori di filtri](data-flow-for-filter-developers.md)
-   [Gestione controllo qualità](quality-control-management.md)
-   [Thread e sezioni critiche](threads-and-critical-sections.md)

**Supporto di COM**

I filtri DirectShow sono oggetti COM, in genere inclusi in una dll. La libreria di classi di base implementa un Framework per supportare COM. Viene descritta nella sezione [DirectShow e com](directshow-and-com.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



