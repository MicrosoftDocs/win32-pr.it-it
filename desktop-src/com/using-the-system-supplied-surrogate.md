---
title: Uso del surrogato System-Supplied
description: Uso del surrogato System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332479"
---
# <a name="using-the-system-supplied-surrogate"></a>Uso del surrogato System-Supplied

Per utilizzare il surrogato fornito dal sistema per il server DLL, registrare la DLL specificando una stringa vuota o **null** per il valore [DllSurrogate](dllsurrogate.md) nel registro di sistema. Quando una richiesta di attivazione per un server DLL designato si avvicina a COM, COM avvia il processo surrogato predefinito e la DLL richiesta (specificando il CLSID nella riga di comando Launch internamente) allo stesso tempo per evitare una chiamata separata. Per informazioni sull'esecuzione di più di un server DLL in un processo surrogato, vedere la pagina relativa alla [condivisione dei surrogati](surrogate-sharing.md).

L'implementazione predefinita del processo surrogato è un server pseudo-COM di tipo modello a thread misto. Quando più server DLL vengono caricati in un singolo processo surrogato, questo processo assicura che venga creata un'istanza di ogni server DLL utilizzando il modello di threading specificato nel registro di sistema per tale server. Tutti i server a thread libero caricati si troveranno insieme nell'apartment multithread, mentre ogni server con threading Apartment si troverà in un Apartment a thread singolo. Se un server DLL supporta entrambi i modelli di threading, COM sceglierà il multithreading.

Questo processo surrogato viene scritto in modo che COM gestisca lo scaricamento dei server DLL e la terminazione del processo surrogato.

Il surrogato fornito dal sistema funziona molto bene per la maggior parte degli sviluppatori, oltre a essere molto facile da usare. Tuttavia, gli sviluppatori con considerazioni speciali possono decidere che è necessario un surrogato personalizzato. Per ulteriori informazioni, vedere [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 




