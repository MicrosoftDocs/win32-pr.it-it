---
title: Uso dei livelli di protezione dell'output
description: Uso dei livelli di protezione dell'output
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, livelli di protezione dell'output (OPL)
- Windows Media Format SDK, livelli di protezione
- Advanced Systems Format (ASF), livelli di protezione dell'output (OPL)
- ASF (Advanced Systems Format), livelli di protezione dell'output (OPL)
- Advanced Systems Format (ASF), livelli di protezione
- ASF (Advanced Systems Format), livelli di protezione
- Advanced Systems Format (ASF), più licenze
- ASF (Advanced Systems Format), più licenze
- digital rights management (DRM), livelli di protezione dell'output (OPL)
- DRM (digital rights management), livelli di protezione dell'output (OPL)
- digital rights management (DRM), livelli di protezione
- DRM (digital rights management),livelli di protezione
- digital rights management (DRM), valutazione dei livelli di protezione dell'output (OPL)
- DRM (digital rights management), valutazione dei livelli di protezione dell'output (OPL)
- digital rights management (DRM), più licenze
- DRM (digital rights management),più licenze
- livelli di protezione dell'output (OPL)
- OPL (livelli di protezione dell'output)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2888891e50ec90e784bf6f4420637544854a9b600b5538e9655bc6d3028f76d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697715"
---
# <a name="working-with-output-protection-levels"></a>Uso dei livelli di protezione dell'output

Le licenze create usando l'SDK Windows Media Rights Manager 10 possono specificare restrizioni di azione usando i livelli di protezione dell'output (OPL). Gli OLS consentono a un autore di licenze di consentire alcune azioni solo nei dispositivi con tecnologie specifiche. I vantaggi dell'uso degli opls sono la maggiore flessibilità nella creazione di restrizioni di licenza rispetto alle versioni precedenti. Inoltre, gli OPL sono espandibili per supportare le tecnologie future. È possibile supportare tali licenze nelle applicazioni usando i metodi [**dell'interfaccia IWMDRMReader2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)

Per leggere i file protetti da una licenza che specifica gli OPL, è necessario controllare l'OPL per l'azione desiderata. La tecnologia di output utilizzata dall'applicazione deve essere consentita dall'OPL nella licenza. Ad esempio, alcune licenze per l'audio protetto potrebbero richiedere l'uso di un percorso audio sicuro per riprodurlo.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configurazione del lettore per valutare i livelli di protezione dell'output

Prima di poter controllare gli OPL per i file caricati nel lettore, è necessario chiamare il metodo [**IWMDRMReader2::SetEvaluateOutputLevelLicenses,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) passando **TRUE** per il *parametro fEvaluate.* Se non si chiama questo metodo, le licenze che richiedono gli OPL non sono visibili all'applicazione.

## <a name="evaluating-copy-output-protection-levels"></a>Valutazione dei livelli di protezione dell'output di copia

Per ottenere i livelli di protezione dell'output per l'azione di copia, chiamare il metodo [**IWMDRMReader2::GetCopyOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) I dati ricevuti dalla chiamata vengono archiviati in una [**struttura \_ \_ OPL DRM COPY.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) La struttura contiene un livello di protezione dell'output di base, che specifica il livello di output minimo per l'azione di copia nella licenza. Tuttavia, la struttura OPL DRM COPY contiene anche due elenchi di identificatori di tecnologia: uno per le tecnologie consentite con un OPL inferiore rispetto alla base e uno per le tecnologie con valutazione uguale o superiore rispetto all'OPL di base, ma che sono limitate dalla \_ \_ licenza. È necessario controllare le inclusioni e le esclusioni per assicurarsi che la tecnologia utilizzata dall'applicazione sia consentita dalla licenza.

## <a name="evaluating-play-output-protection-levels"></a>Valutazione dei livelli di protezione dell'output di riproduzione

Per ottenere i livelli di protezione dell'output per l'azione di riproduzione, chiamare il metodo [**IWMDRMReader2::GetPlayOutputLevels.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) I dati ricevuti dalla chiamata vengono archiviati in una [**struttura \_ \_ OPL DRM PLAY.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) La struttura contiene diverse altre strutture. I livelli di protezione dell'output di base per l'azione di riproduzione vengono archiviati in una struttura [**DRM \_ MINIMUM OUTPUT \_ PROTECTION \_ \_ LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (il membro **minOPL** di **DRM PLAY \_ \_ OPL),** che definisce l'OPL minimo necessario per riprodurre il contenuto in diversi formati. È necessario controllare il membro per il tipo di formati di output che l'applicazione fornisce.

La **struttura \_ \_ OPL DRM PLAY** definisce due tipi di restrizioni: il campionamento in basso richiesto e gli identificatori di protezione dell'output video consentiti.

Il campionamento a discesa richiesto è definito come un elenco di identificatori della tecnologia di output (il membro **oplIdDownsample** di **DRM \_ PLAY \_ OPL)** che, se usato, può ricevere il contenuto per la riproduzione solo se il contenuto viene prima sottocampionato a una velocità in bit inferiore.

Gli identificatori di protezione dell'output video consentiti sono definiti come un elenco di tecnologie di output video con informazioni di configurazione per ognuno.

## <a name="handling-multiple-licenses"></a>Gestione di più licenze

Ad alcuni file possono essere associate più licenze nell'archivio licenze locale. Quando si valutano gli OPL per un file che si sta leggendo, è possibile verificare la presenza di licenze aggiuntive chiamando il metodo [**IWMDRMReader2::TryNextLicense.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) È consigliabile continuare a provare le licenze finché non ne viene individuata una che consenta l'azione da eseguire o finché TryNextLicense non restituisce DRM S FALSE, che indica che non sono presenti \_ \_ altre licenze.

In alcuni casi, un file potrebbe avere una licenza associata che richiede un OPL che l'applicazione non è in grado di supportare. In tal caso è importante verificare la presenza di licenze aggiuntive perché potrebbe esistere una licenza che non specifica gli OPL.

**Nota** DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




