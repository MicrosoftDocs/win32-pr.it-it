---
description: L'API XAPO consente la creazione di oggetti di elaborazione audio multipiattaforma (XAPO) da usare in XAudio2 sia Windows che Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Panoramica di XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ee64e865c8e3ef3cdac026274b922db438a54979dcb30d855a92b96e4e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589911"
---
# <a name="xapo-overview"></a>Panoramica di XAPO

L'API XAPO consente la creazione di oggetti di elaborazione audio multipiattaforma (XAPO) da usare in XAudio2 sia Windows che Xbox 360. Un XAPO è un oggetto che accetta i dati audio in ingresso ed esegue un'operazione sui dati prima di passarlo. È possibile usare un XAPO per eseguire un'ampia gamma di attività, tra cui l'aggiunta di riverbero a un flusso audio e il monitoraggio dei livelli di volume di picco.

## <a name="creating-new-xapos"></a>Creazione di nuovi XAPO

L'API XAPO fornisce [**l'interfaccia IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e la [**classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) per la creazione di nuovi tipi XAPO. **L'interfaccia IXAPO** contiene tutti i metodi che devono essere implementati per creare un nuovo XAPO. La **classe CXAPOBase** fornisce un'implementazione di base **dell'interfaccia IXAPO.** **CXAPOBase** implementa tutti i metodi di interfaccia **IXAPO,** ad eccezione del metodo [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) univoco per ogni XAPO.

Per un esempio di creazione di un nuovo XAPO, vedere [Procedura: Creare un XAPO.](how-to--create-an-xapo.md)

Per un esempio di creazione di un XAPO che accetta parametri di run-time, vedere Procedura: Aggiungere il supporto dei parametri di [run-time a un XAPO.](how-to--add-run-time-parameter-support-to-an-xapo.md)

## <a name="xapos-and-com"></a>XAPO e COM

Gli XAPO implementano **l'interfaccia IUnknown.** Le [**interfacce IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) includono i tre metodi **IUnknown:** **QueryInterface,** **AddRef** e **Release.** [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornisce implementazioni di tutti e tre i metodi IUnknown. Una nuova istanza di **CXAPOBase** avrà un conteggio dei riferimenti di 1. Verrà eliminato quando il conteggio dei riferimenti diventa 0. Le implementazioni **di IXAPO** e **IXAPOParameters** devono seguire lo stesso modello per consentire la gestione corretta quando vengono usate con XAudio2.

Le istanze XAPO vengono passate a XAudio2 **come interfacce IUnknown.** XAudio2 usa **QueryInterface per** acquisire un'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e per rilevare se XAPO implementa l'interfaccia [**IXAPOParameters.**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) Le implementazioni **di IXAPO** devono accettare richieste **\_ \_ per uuidof(IXAPO).** Se **IXAPOParameters è** implementato, deve accettare anche le richieste per **\_ \_ uuidof(IXAPOParameters).**

## <a name="using-an-xapo-in-xaudio2"></a>Uso di XAPO in XAudio2

Gli XAPO vengono usati in XAudio2 collegandoli alle voci. Ogni voce XAudio2 ha una catena di effetti contenente zero o più effetti audio. I dati audio inviati a una voce vengono passati attraverso ogni effetto nella catena prima di essere inviati alle destinazioni di output della voce. I dati vengono passati dalla voce a ogni effetto usando il *parametro pInputProcessParameters* del [**metodo IXAPO::P rocess.**](/windows/win32/api/xapo/nf-xapo-ixapo-process) Viene quindi restituita alla voce usando il *parametro pOutputProcessParameters.* La voce accetta l'output di ogni effetto e lo alimenta nell'effetto successivo nella catena finché non viene lasciato alcun effetto nella catena.

Per altre informazioni sulle catene di effetti XAudio2, vedere [Effetti audio XAudio2.](xaudio2-audio-effects.md)

Per un esempio dell'uso di un XAPO in XAudio2, vedere [Procedura: Usare un XAPO in XAudio2.](how-to--use-an-xapo-in-xaudio2.md)

## <a name="effect-libraries"></a>Librerie degli effetti

La libreria degli effetti XAPO contiene diversi XAPO e un metodo comune per crearne un'istanza. Per [informazioni su XAPOFX,](xapofx-overview.md) vedere Panoramica di XAPOFX. XAudio2 include anche effetti di riverbero e misurazione del volume predefiniti. Per altre informazioni sugli effetti XAudio2 predefiniti, vedere Effetti audio [XAudio2.](xaudio2-audio-effects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Effetti audio di XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
