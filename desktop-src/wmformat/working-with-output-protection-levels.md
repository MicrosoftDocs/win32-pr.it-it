---
title: Utilizzo dei livelli di protezione dell'output
description: Utilizzo dei livelli di protezione dell'output
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, livelli di protezione dell'output (OPL)
- Windows Media Format SDK, livelli di protezione
- ASF (Advanced Systems Format), livelli di protezione dell'output (OPL)
- ASF (formato avanzato dei sistemi), livelli di protezione dell'output (OPL)
- ASF (Advanced Systems Format), livelli di protezione
- ASF (formato avanzato dei sistemi), livelli di protezione
- ASF (Advanced Systems Format), più licenze
- ASF (Advanced Systems Format), più licenze
- Digital Rights Management (DRM), livelli di protezione dell'output (OPL)
- DRM (Digital Rights Management), livelli di protezione dell'output (OPL)
- Digital Rights Management (DRM), livelli di protezione
- DRM (Digital Rights Management), livelli di protezione
- Digital Rights Management (DRM), valutazione del livello di protezione dell'output (OPL)
- DRM (Digital Rights Management), valutazione del livello di protezione dell'output (OPL)
- Digital Rights Management (DRM), più licenze
- DRM (Digital Rights Management), più licenze
- livelli di protezione dell'output (OPL)
- OPL (livelli di protezione dell'output)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336257"
---
# <a name="working-with-output-protection-levels"></a>Utilizzo dei livelli di protezione dell'output

Le licenze create mediante Windows Media Rights Manager 10 SDK possono specificare restrizioni di azione mediante i livelli di protezione dell'output (OPLs). OPLs consente a un creatore di licenze di consentire alcune azioni solo sui dispositivi con tecnologie specifiche. I vantaggi dell'uso di OPLs sono la maggiore flessibilità nella creazione di restrizioni di licenza rispetto alle versioni precedenti. Inoltre, OPLs sono espandibili per supportare le tecnologie future. È possibile supportare tali licenze nelle applicazioni usando i metodi dell'interfaccia [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .

Per leggere i file protetti da una licenza che specifica OPLs, è necessario controllare il OPL per l'azione desiderata. La tecnologia di output usata dall'applicazione deve essere consentita da OPL nella licenza. Ad esempio, alcune licenze per l'audio protetto potrebbero richiedere l'uso di un percorso audio sicuro per riprodurlo.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Configurazione del lettore per valutare i livelli di protezione dell'output

Prima di poter controllare OPLs per i file caricati nel lettore, è necessario chiamare il metodo [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , passando **true** per il parametro *fEvaluate* . Se non si chiama questo metodo, le licenze che richiedono OPLs non sono visibili per l'applicazione.

## <a name="evaluating-copy-output-protection-levels"></a>Valutazione del livello di protezione dell'output di copia

Per ottenere i livelli di protezione dell'output per l'azione di copia, chiamare il metodo [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) . I dati ricevuti dalla chiamata vengono archiviati in una struttura di [**\_ Copia \_ OPL di DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) . La struttura contiene un livello di protezione dell'output di base che specifica il livello di output minimo per l'azione di copia nella licenza. Tuttavia, la \_ \_ struttura OPL copia DRM contiene anche due elenchi di identificatori di tecnologia: uno per le tecnologie consentite classificate a una OPL inferiore rispetto alla base e uno per le tecnologie classificate come uguale o superiore rispetto al OPL di base ma che sono limitate dalla licenza. È necessario controllare le inclusioni e le esclusioni per assicurarsi che la tecnologia usata dall'applicazione sia consentita dalla licenza.

## <a name="evaluating-play-output-protection-levels"></a>Valutazione del livello di protezione dell'output di riproduzione

Per ottenere i livelli di protezione dell'output per l'azione Play, chiamare il metodo [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) . I dati ricevuti dalla chiamata vengono archiviati in una struttura [**OPL di \_ riproduzione \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) . La struttura contiene diverse altre strutture. I livelli di protezione dell'output di base per l'azione di riproduzione vengono archiviati in una struttura di livello di  [**\_ \_ \_ protezione \_ dell'output minimo DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (il membro minOPL di **DRM \_ Play \_ OPL**), che definisce il OPL minimo necessario per riprodurre il contenuto in una varietà di formati. È necessario controllare il membro per il tipo di formati di output che l'applicazione recapita.

La **struttura \_ \_ OPL di riproduzione DRM** definisce due tipi di restrizioni: il campionamento inattivo richiesto e gli identificatori di protezione dell'output video consentiti.

Il sottocampionamento richiesto è definito come un elenco di identificatori di tecnologia di output (il membro **oplIdDownsample** di **DRM \_ Play \_ OPL**) che, se usato, può ricevere il contenuto per la riproduzione solo se il contenuto viene prima sottoposto a campionamento a una velocità in bit inferiore.

Gli identificatori di protezione dell'output video consentiti sono definiti come un elenco di tecnologie di output video con le informazioni di configurazione per ognuna.

## <a name="handling-multiple-licenses"></a>Gestione di più licenze

Alcuni file possono avere più licenze associate nell'archivio licenze locale. Quando si valuta OPLs per un file che si sta leggendo, è possibile verificare la presenza di licenze aggiuntive chiamando il metodo [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) . È necessario continuare a provare le licenze fino a quando non ne viene individuato uno che consente l'azione da eseguire o fino a quando TryNextLicense non restituisce DRM \_ S \_ false, che indica che non sono presenti altre licenze.

In alcuni casi, è possibile che un file disponga di una licenza associata che richiede un OPL che l'applicazione non può supportare. In tal caso è importante verificare la presenza di licenze aggiuntive perché potrebbe esistere una licenza che non specifica OPLs.

**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaccia IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




