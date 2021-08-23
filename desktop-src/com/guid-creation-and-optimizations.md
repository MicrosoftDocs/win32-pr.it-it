---
title: Creazione e ottimizzazioni di GUID
description: Creazione e ottimizzazioni di GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731431"
---
# <a name="guid-creation-and-optimizations"></a>Creazione e ottimizzazioni di GUID

Poiché un CLSID, come un identificatore di interfaccia (IID), è un GUID, nessun'altra classe, indipendentemente da chi lo scrive, ha un CLSID duplicato. Gli implementatori del server ottengono in genere i CLSID tramite [**la funzione CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) Questa funzione garantisce la produzione di CLSID univoci, in modo che gli implementatori di server in tutto il mondo possano sviluppare e distribuire il software in modo indipendente senza il rischio di collisioni accidentali con il software scritto da altri utenti.

L'uso di CLSID univoci evita la possibilità di conflitti di nomi tra classi perché i CLSID non sono in alcun modo connessi ai nomi usati nell'implementazione sottostante. Ad esempio, due fornitori diversi possono scrivere classi denominate "StackClass", ma ognuna avrebbe un CLSID univoco e quindi non poteva essere confusa.

COM deve spesso eseguire il mapping di GUID (ID e CLSID) a un set arbitrariamente grande di altri valori. Gli sviluppatori di applicazioni possono velocizzare tali ricerche e quindi migliorare le prestazioni del sistema, generando i GUID per l'applicazione come blocco di valori consecutivi.

Il modo più efficiente per generare un blocco di GUID consecutivi è eseguire l'utilità uuidgen usando le opzioni -n e -x, che genera un blocco di UUID, ognuno dei quali il cui primo valore DWORD viene incrementato di uno.

Ad esempio, se si digita

**uuidgen -n5 -x**

L'utilità uuidgen genererà un blocco di UUID simile al seguente:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Un metodo per generare e tenere traccia dei GUID per un intero progetto inizia con la generazione di un blocco di un numero arbitrariamente elevato di UUID, ad esempio 500. Ad esempio, se si digita

**uuidgen -n500 -x > guids.txt**

L'utilità genererà 500 UUID consecutivi e li scriverà nel file di testo specificato. È quindi possibile archiviare questo file nell'albero di origine, fornendo un singolo repository per tutti i GUID da usare in un progetto. Poiché gli utenti richiedono GUID per le parti del progetto, possono estrarre il file, prendere tutti i GUID necessari, contrassegnandoli come presi e lasciando una nota sulla posizione nel codice o nella "specifica" in cui vengono utilizzati.

Oltre a migliorare le prestazioni del sistema, la generazione di blocchi di GUID consecutivi in questo modo offre i vantaggi seguenti:

-   Un file centrale contenente tutti i GUID per un'applicazione consente di tenere traccia facilmente di quali GUID sono relativi a cosa e quali utenti li usano.
-   Un blocco di GUID consecutivi associati a una particolare applicazione consente a sviluppatori e tester di riconoscere i GUID interni durante il debug e di trovarli nel Registro di sistema perché vengono archiviati in sequenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità del server COM](com-server-responsibilities.md)
</dt> </dl>

 

 




