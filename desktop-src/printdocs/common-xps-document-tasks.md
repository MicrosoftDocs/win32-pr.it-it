---
description: In questa pagina sono elencate alcune delle attività di programmazione comunemente eseguite con l'API del documento XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Attività comuni di programmazione di documenti XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311830"
---
# <a name="common-xps-document-programming-tasks"></a>Attività comuni di programmazione di documenti XPS

In questa pagina sono elencate alcune delle attività di programmazione comunemente eseguite con l'API del documento XPS.

## <a name="common-xps-document-tasks"></a>Attività comuni relative ai documenti XPS

Negli esempi di codice seguenti vengono illustrate alcune delle attività di programmazione che vengono in genere eseguite quando l'API del documento XPS viene utilizzata per l'utilizzo di un OM XPS.

<dl>

[Inizializzare un OM XPS](xps-object-model-initialization.md)  
[Creazione di un OM XPS vuoto](create-a-blank-xps-om.md)  
[Leggere un documento XPS in un OM XPS](read-an-xps-document-into-an-xps-om.md)  
[Esplorare XPS OM](navigate-the-xps-om.md)  
[Scrivere testo in un OM XPS](write-text-to-an-xps-om.md)  
[Creare grafica in un OM XPS](draw-graphics-in-an-xps-om.md)  
[Inserire immagini in un OM XPS](place-images-in-an-xps-om.md)  
[Scrivere un OM XPS in un documento XPS](write-an-xps-om-to-an-xps-document.md)  
[Stampare un OM XPS](print-an-xps-om.md)  
[Uso delle interfacce di raccolta OM XPS](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Dichiarazione di non responsabilità

Gli esempi di codice non sono destinati a essere programmi completi e funzionanti. Gli esempi di codice a cui si fa riferimento in questa pagina, ad esempio, non eseguono il controllo dei parametri, il controllo degli errori o la gestione degli errori. Usare questi esempi come punto di partenza e quindi aggiungere il codice necessario per creare un'applicazione affidabile. Per ulteriori informazioni sui valori restituiti **HRESULT** e sulle strategie di gestione degli errori, vedere [gestione degli errori in com](../com/error-handling-in-com.md).

Prima di poter utilizzare le interfacce XPS OM, è necessario inizializzare COM nel thread, come illustrato nel codice di esempio seguente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Per maggiore chiarezza, questi esempi di codice usano un OM XPS molto semplice, uno che potrebbe non essere sufficientemente complesso per l'applicazione. Come esempio, negli esempi di codice che aggiungono contenuto a una pagina gli elementi visivi di una pagina vengono aggiunti direttamente all'elenco di oggetti visivi della pagina; in pratica, tuttavia, è possibile raggruppare gli oggetti visivi in oggetti Canvas, in modo che sia possibile agire su più oggetti come un gruppo. Pertanto, per abilitare il supporto dello stesso contenuto per più di una dimensione di pagina, è possibile raggruppare il contenuto visivo di una pagina in un singolo oggetto Canvas, quindi applicare una trasformazione all'area di disegno per adattarla alle dimensioni correnti della pagina.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
