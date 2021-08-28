---
title: Uso del System-Supplied surrogato
description: Uso del System-Supplied surrogato
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0faec7c57f0e2010d0e817a4e44b81d65ad207371b591296bea2354307c7b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243431"
---
# <a name="using-the-system-supplied-surrogate"></a>Uso del System-Supplied surrogato

Per usare il surrogato fornito dal sistema per il server DLL, registrare la DLL specificando una stringa vuota o **NULL** per il [valore DllSurrogate](dllsurrogate.md) nel Registro di sistema. Quando una richiesta di attivazione per un server DLL designato arriva a COM, COM avvia il processo surrogato predefinito e la DLL richiesta (specificando internamente il CLSID nella riga di comando di avvio) per evitare una chiamata separata. Per informazioni sull'esecuzione di più di un server DLL in un processo surrogato, vedere [Condivisione di surrogati.](surrogate-sharing.md)

L'implementazione predefinita del processo surrogato è un server pseudo-COM in stile modello a threading misto. Quando più server DLL vengono caricati in un singolo processo surrogato, questo processo garantisce la creazione di un'istanza di ogni server DLL usando il modello di threading specificato nel Registro di sistema per tale server. Tutti i server a thread libero caricati si conviverranno nell'apartment multithreading, mentre ogni server con thread apartment risiederà in un apartment a thread singolo. Se un server DLL supporta entrambi i modelli di threading, COM sceglierà il multithreading.

Questo processo surrogato viene scritto in modo che COM gestisca sia lo scaricamento dei server DLL che la terminazione del processo surrogato.

Il surrogato fornito dal sistema funzionerà molto bene per la maggior parte degli sviluppatori, oltre a essere molto facile da usare. Tuttavia, gli sviluppatori con considerazioni speciali possono decidere che è necessario un surrogato personalizzato. Per altre informazioni, vedere [Scrittura di un surrogato personalizzato.](writing-a-custom-surrogate.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> </dl>

 

 




