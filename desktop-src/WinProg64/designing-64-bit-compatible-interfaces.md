---
title: Progettazione di interfacce compatibili con 64 bit
description: I problemi di compatibilità con le versioni precedenti si verificano quando si aggiungono nuovi tipi di dati o metodi a un'interfaccia, si modificano i tipi di dati obsoleti o si utilizzano i tipi di dati
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- Programmazione Windows con compatibilità con le versioni precedenti a 64 bit
- interfacce a 64 bit compatibili con la programmazione Windows a 64 bit
- Guida alla programmazione di Windows a 64 bit, programmazione Windows a 64 bit, compatibilità
- compatibilità con la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329812"
---
# <a name="designing-64-bit-compatible-interfaces"></a>Progettazione di interfacce compatibili con 64 bit

Il porting da Windows a 32 bit a Windows a 64 bit non dovrebbe, da solo, creare eventuali problemi per le applicazioni distribuite, indipendentemente dal fatto che usino chiamate a procedure remote (RPC) direttamente o tramite DCOM. Il modello di programmazione RPC specifica le dimensioni dei dati ben definite e i tipi integer con le stesse dimensioni a ogni estremità della connessione. Inoltre, nel modello di dati LLP64 abstract sviluppato per Windows a 64 bit, solo i puntatori si espandono a 64 bit. tutti gli altri tipi di dati Integer rimangono 32 bit. Poiché i puntatori sono locali a ogni lato della connessione client/server e vengono in genere trasmessi come marcatori **null** o non **null** , il motore di marshalling è in grado di gestire in modo trasparente diverse dimensioni del puntatore a una delle estremità di una connessione.

Tuttavia, si verificano problemi di compatibilità con le versioni precedenti quando si aggiungono nuovi tipi di dati o metodi a un'interfaccia, si modificano i tipi di dati obsoleti o si utilizzano i tipi di dati in modo Negli argomenti seguenti viene illustrato come evitare queste situazioni, se possibile, e come progettare soluzioni alternative affidabili quando non è possibile evitarle.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Modifica di un'interfaccia esistente](changing-an-existing-interface.md)
-   [Evitare le informazioni nascoste](avoiding-information-hiding.md)
-   [Evitare il polimorfismo](avoiding-polymorphism.md)
-   [Uso di nuovi tipi di dati nel file IDL](using-new-data-types-in-your-idl-file.md)
-   [Preparazione dell'applicazione per Windows a 64 bit](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>Sezioni correlate

Se non si ha già familiarità con i nuovi tipi di dati, l'ambiente di lavoro e le modifiche dell'API per Windows a 64 bit, vedere [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).

 

 




