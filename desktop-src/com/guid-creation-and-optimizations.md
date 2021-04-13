---
title: Creazione e ottimizzazioni di GUID
description: Creazione e ottimizzazioni di GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396778"
---
# <a name="guid-creation-and-optimizations"></a>Creazione e ottimizzazioni di GUID

Poiché un CLSID, come un identificatore di interfaccia (IID), è un GUID, nessun'altra classe, indipendentemente da chi lo scrive, presenta un CLSID duplicato. Gli implementatori del server in genere ottengono CLSID tramite la funzione [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) . Questa funzione garantisce la produzione di CLSID univoci, in modo che gli implementatori di server in tutto il mondo possano sviluppare e distribuire il software in modo indipendente senza temere conflitti accidentali con il software scritto da altri.

L'utilizzo di CLSID univoci consente di evitare la possibilità di conflitti di nomi tra le classi, perché i CLSID non sono in alcun modo connessi ai nomi utilizzati nell'implementazione sottostante. Ad esempio, due fornitori diversi possono scrivere classi denominate "StackClass", ma ognuna avrà un CLSID univoco e pertanto non può essere confusa.

COM spesso deve eseguire il mapping dei GUID (IID e CLSID) a un set arbitrariamente grande di altri valori. Gli sviluppatori di applicazioni possono velocizzare le ricerche e migliorare le prestazioni del sistema generando i GUID per l'applicazione come un blocco di valori consecutivi.

Il modo più efficiente per generare un blocco di GUID consecutivi consiste nell'eseguire l'utilità uuidgen usando le opzioni-n e-x, che generano un blocco di UUID, ciascuno dei quali il primo valore DWORD viene incrementato di uno.

Ad esempio, se si digita

**uuidgen-N5-x**

l'utilità uuidgen genera un blocco di UUID analogo al seguente:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Un metodo per generare e tenere traccia dei GUID per un intero progetto inizia con la generazione di un blocco di un numero arbitrariamente elevato di UUID, ad indicare 500. Ad esempio, se si digita

**uuidgen-N500-x > guids.txt**

l'utilità genera 500 UUID consecutivi e li scrive nel file di testo specificato. È quindi possibile controllare questo file nell'albero di origine, fornendo un unico repository per tutti i GUID da usare in un progetto. Poiché gli utenti necessitano di GUID per le parti del progetto, possono estrarre il file, usare tuttavia molti GUID necessari, contrassegnarli come presi e lasciare una nota sul punto in cui si trovano nel codice o "spec".

Oltre a migliorare le prestazioni del sistema, la generazione di blocchi di GUID consecutivi in questo modo presenta i vantaggi seguenti:

-   Un file centrale che contiene tutti i GUID di un'applicazione consente di tenere traccia di quali GUID sono relativi a cosa e quali utenti li usano.
-   Un blocco di GUID consecutivi associati a una particolare applicazione consente agli sviluppatori e ai tester di riconoscere i GUID interni durante il debug e di individuarli più facilmente nel registro di sistema perché vengono archiviati in modo sequenziale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> </dl>

 

 




