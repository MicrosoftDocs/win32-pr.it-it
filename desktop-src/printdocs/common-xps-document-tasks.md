---
description: Questa pagina elenca alcune delle attività di programmazione comunemente eseguite con l'API documento XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Attività comuni di programmazione di documenti XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7f71614344968bcc68e658021e1f34296a595d9fbf58be2d544c03c3dc428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846351"
---
# <a name="common-xps-document-programming-tasks"></a>Attività comuni di programmazione di documenti XPS

Questa pagina elenca alcune delle attività di programmazione comunemente eseguite con l'API documento XPS.

## <a name="common-xps-document-tasks"></a>Attività comuni dei documenti XPS

Gli esempi di codice seguenti illustrano alcune delle attività di programmazione comunemente eseguite quando l'API documento XPS viene usata per l'uso di un sistema operativo XPS.

<dl>

[Inizializzare un sistema operativo XPS](xps-object-model-initialization.md)  
[Creare un sistema operativo XPS vuoto](create-a-blank-xps-om.md)  
[Leggere un documento XPS in un sistema operativo XPS](read-an-xps-document-into-an-xps-om.md)  
[Esplorare xps OM](navigate-the-xps-om.md)  
[Scrivere testo in un sistema operativo XPS](write-text-to-an-xps-om.md)  
[Disegnare grafica in un sistema operativo XPS](draw-graphics-in-an-xps-om.md)  
[Inserire immagini in un sistema operativo XPS](place-images-in-an-xps-om.md)  
[Scrivere un file OM XPS in un documento XPS](write-an-xps-om-to-an-xps-document.md)  
[Stampare un sistema operativo XPS](print-an-xps-om.md)  
[Uso delle interfacce di raccolta OM XPS](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Dichiarazione di non responsabilità

Gli esempi di codice non sono destinati a essere programmi completi e funzionanti. Gli esempi di codice a cui si fa riferimento in questa pagina, ad esempio, non eseguono il controllo dei parametri, il controllo degli errori o la gestione degli errori. Usare questi esempi come punto di partenza e quindi aggiungere il codice necessario per creare un'applicazione affidabile. Per altre informazioni sui **valori restituiti HRESULT** e sulle strategie di gestione degli errori, vedere [Gestione degli errori in COM](../com/error-handling-in-com.md).

Prima di poter usare le interfacce OM XPS, è necessario inizializzare COM nel thread, come illustrato nel codice di esempio seguente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Per maggiore chiarezza, questi esempi di codice usano un sistema operativo XPS molto semplice, che potrebbe non essere sufficientemente complesso per l'applicazione. Come un caso specifico, negli esempi di codice che aggiungono contenuto a una pagina, gli elementi visivi di una pagina vengono aggiunti direttamente all'elenco di oggetti visivi della pagina; in pratica, tuttavia, potrebbe essere necessario raggruppare gli oggetti visivi in oggetti canvas, in modo che più oggetti potrebbero essere gestiti come un gruppo. Di conseguenza, per abilitare il supporto dello stesso contenuto per più di una dimensione di pagina, è possibile raggruppare il contenuto visivo di una pagina in un singolo oggetto canvas e quindi applicare una trasformazione all'area di disegno per ridimensionarlo in base alle dimensioni correnti della pagina.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
