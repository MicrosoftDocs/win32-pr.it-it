---
description: L'API XAPO consente la creazione di XAPO (Multi-Platform Audio Processing Objects) per l'uso in XAudio2 in Windows e Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Panoramica di XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319075"
---
# <a name="xapo-overview"></a>Panoramica di XAPO

L'API XAPO consente la creazione di XAPO (Multi-Platform Audio Processing Objects) per l'uso in XAudio2 in Windows e Xbox 360. Un XAPO è un oggetto che accetta i dati audio in ingresso ed esegue alcune operazioni sui dati prima di passarli. È possibile usare un XAPO per eseguire una serie di attività, tra cui l'aggiunta di Reverb a un flusso audio e il monitoraggio dei livelli di picco del volume.

## <a name="creating-new-xapos"></a>Creazione di un nuovo XAPOs

L'API XAPO fornisce l'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) per la compilazione di nuovi tipi XAPO. L'interfaccia **IXAPO** contiene tutti i metodi che devono essere implementati per creare un nuovo XAPO. La classe **CXAPOBase** fornisce un'implementazione di base dell'interfaccia **IXAPO** . **CXAPOBase** implementa tutti i metodi dell'interfaccia **IXAPO** ad eccezione del metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , che è univoco per ogni XAPO.

Per un esempio di creazione di un nuovo XAPO, vedere [procedura: creare un XAPO](how-to--create-an-xapo.md).

Per un esempio di creazione di un XAPO che accetta i parametri di runtime, vedere [procedura: aggiungere il supporto dei parametri in fase di esecuzione a un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs e COM

XAPOs implementano l'interfaccia **IUnknown** . Le interfacce [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) includono i tre metodi **IUnknown** : **QueryInterface**, **AddRef** e **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornisce implementazioni di tutti e tre i metodi IUnknown. Una nuova istanza di **CXAPOBase** avrà un conteggio dei riferimenti pari a 1. Verrà eliminato definitivamente quando il conteggio dei riferimenti diventa 0. Le implementazioni di **IXAPO** e **IXAPOParameters** devono seguire lo stesso modello per consentire la corretta gestione quando vengono usate con XAudio2.

Le istanze di XAPO vengono passate a XAudio2 come interfacce **IUnknown** . XAudio2 utilizza **QueryInterface** per acquisire un'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e per rilevare se XAPO implementa l'interfaccia [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . Le implementazioni di **IXAPO** devono accettare richieste per **\_ \_ uuidof (IXAPO)**. Se **IXAPOParameters** è implementato, deve accettare anche le richieste per **\_ \_ uuidof (IXAPOParameters)**.

## <a name="using-an-xapo-in-xaudio2"></a>Uso di un XAPO in XAudio2

XAPOs vengono utilizzati in XAudio2 mediante la connessione a voci. Ogni voce di XAudio2 ha una catena di effetti che contiene zero o più effetti audio. I dati audio inviati a una voce vengono passati attraverso ogni effetto della catena prima che vengano inviati alle destinazioni di output della voce. I dati vengono passati dalla voce a ogni effetto usando il parametro *pInputProcessParameters* del metodo [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) . Viene quindi restituito alla voce usando il parametro *pOutputProcessParameters* . La voce prende l'output di ogni effetto e la inserisce nell'effetto successivo della catena fino a quando non vengono lasciati effetti nella catena.

Per altre informazioni sulle catene di effetti XAudio2, vedere [effetti audio XAudio2](xaudio2-audio-effects.md).

Per un esempio dell'uso di un XAPO in XAudio2, vedere [procedura: usare un XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Librerie degli effetti

La libreria degli effetti XAPO contiene diversi XAPOs e un metodo comune per crearne un'istanza. Per informazioni su XAPOFX, vedere [Panoramica di XAPOFX](xapofx-overview.md) . Inoltre, XAudio2 include effetti predefiniti del contatore e del contatore del volume. Per ulteriori informazioni sugli effetti XAudio2 predefiniti, vedere [XAudio2 Audio Effects](xaudio2-audio-effects.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Effetti audio di XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
