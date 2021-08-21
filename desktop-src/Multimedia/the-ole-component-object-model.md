---
title: Oggetto OLE Component Object Model
description: Oggetto OLE Component Object Model
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de83641250c912efbe92d7181deb52b477af06e2b49598ee63762488a932687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805021"
---
# <a name="the-ole-component-object-model"></a>Oggetto OLE Component Object Model

Gli oggetti usati dalla libreria AVIFile fanno tutti parte del Component Object Model OLE. In primo luogo, ciò significa che condividono determinati metodi che li rendono più facili da usare e i valori restituiti sono comuni alla maggior parte dei metodi dell'interfaccia OLE.

L'Component Object Model OLE dei gestori di file e di flusso usa l'interfaccia OLE **IClassFactory** per creare istanze della relativa classe di oggetti. Come oggetti componente, implementano [l'interfaccia IUnknown,](/windows/win32/api/unknwn/nn-unknwn-iunknown) costituita dai [**metodi QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)e [**AddRef.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) **L'interfaccia IUnknown** consente a un'applicazione di ottenere puntatori ad altre interfacce supportate dallo stesso oggetto.

È possibile determinare se un oggetto supporta un'interfaccia specifica usando il **metodo QueryInterface.** Se un oggetto supporta un'interfaccia specificata, **QueryInterface** restituisce un puntatore a tale interfaccia.

È possibile incrementare e decrementare il conteggio dei riferimenti associato a un oggetto usando i [**metodi AddRef**](/previous-versions//dd757100(v=vs.85)) [**e Release.**](/previous-versions//dd757102(v=vs.85)) Il conteggio dei riferimenti consente a più client di accedere a un oggetto. Quando un oggetto viene usato dalla prima applicazione, il conteggio dei riferimenti viene impostato su 1. Le applicazioni usano successivamente il **metodo AddRef** per incrementare il conteggio in modo che l'oggetto tenga traccia del numero di volte in cui è stato eseguito l'accesso.

Quando un'applicazione viene eseguita usando un oggetto , chiama il **metodo Release** per decrementare il conteggio dei riferimenti. Quando il conteggio dei riferimenti è zero, l'oggetto non è più necessario e **Release** libera tutte le risorse che usa ed elimina l'oggetto. Poiché un oggetto usa risorse interne trasparenti per l'applicazione, l'oggetto è responsabile della liberatura. Ad esempio, un gestore di file potrebbe dover chiudere i file su disco aperti e liberare memoria buffer al momento del rilascio.

La maggior parte dei metodi di interfaccia OLE restituiscono handle di risultato definiti tramite il **tipo di dati HRESULT.** Questo tipo di dati è costituito da un codice di gravità, informazioni contestuali, un codice di struttura e un codice di stato. Handle del risultato restituito che indica che l'esito positivo ha il valore zero. Un valore diverso da zero indica un errore e il membro del codice di stato dell'handle del risultato restituito fornisce una base per un'interpretazione aggiuntiva. Per altre informazioni sugli handle dei risultati restituiti OLE, vedere riferimento *per programmatori OLE*.

 

 