---
title: OLE Component Object Model
description: OLE Component Object Model
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103963554"
---
# <a name="the-ole-component-object-model"></a>OLE Component Object Model

Gli oggetti utilizzati dalla libreria AVIFile fanno tutti parte dell'Component Object Model OLE. Principalmente, ciò significa che condividono determinati metodi che ne semplificano l'utilizzo e i valori restituiti sono comuni alla maggior parte dei metodi dell'interfaccia OLE.

Il Component Object Model OLE dei gestori di file e flussi utilizza l'interfaccia OLE **IClassFactory** per creare istanze della relativa classe di oggetti. Come oggetti componente, implementano l'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , che è costituita dai metodi [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)e [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . L'interfaccia **IUnknown** consente a un'applicazione di ottenere puntatori ad altre interfacce supportate dallo stesso oggetto.

È possibile determinare se un oggetto supporta un'interfaccia specifica utilizzando il metodo **QueryInterface** . Se un oggetto supporta un'interfaccia specificata, **QueryInterface** restituisce un puntatore a tale interfaccia.

È possibile incrementare e decrementare il conteggio dei riferimenti associato a un oggetto usando i metodi [**AddRef**](/previous-versions//dd757100(v=vs.85)) e [**Release**](/previous-versions//dd757102(v=vs.85)) . Il conteggio dei riferimenti consente a più client di accedere a un oggetto. Quando un oggetto viene utilizzato dalla prima applicazione, il relativo conteggio dei riferimenti viene impostato su 1. Le applicazioni utilizzeranno successivamente il metodo **AddRef** per incrementare il conteggio per consentire all'oggetto di tenere traccia del numero di volte in cui si accede.

Quando un'applicazione viene eseguita utilizzando un oggetto, viene chiamato il metodo di **rilascio** per decrementare il conteggio dei riferimenti. Quando il conteggio dei riferimenti è pari a zero, l'oggetto non è più necessario e la **versione** libera tutte le risorse utilizzate ed Elimina definitivamente l'oggetto. Poiché un oggetto usa le risorse interne trasparenti per l'applicazione, l'oggetto è responsabile della loro liberazione. Un gestore di file, ad esempio, potrebbe dover chiudere i file aperti del disco e liberare memoria del buffer al momento del rilascio.

La maggior parte dei metodi dell'interfaccia OLE restituiscono handle di risultati definiti utilizzando il tipo di dati **HRESULT** . Questo tipo di dati è costituito da un codice di gravità, da informazioni contestuali, da un codice di struttura e da un codice di stato. Un handle di risultato restituito che indica l'esito positivo ha il valore zero. Un valore diverso da zero indica un errore e il membro del codice di stato dell'handle del risultato restituito fornisce una base per un'interpretazione aggiuntiva. Per ulteriori informazioni sugli handle dei risultati restituiti OLE, vedere la Guida *di riferimento per programmatori OLE*.

 

 