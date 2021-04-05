---
title: Opzioni di class factory
description: Opzioni di class factory
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730431"
---
# <a name="class-factory-options"></a>Opzioni di class factory

Un controllo ActiveX, in virtù di un oggetto COM, deve disporre di codice server associato che supporta la creazione di controlli tramite [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) come minimo.

È facoltativo, non obbligatorio, che questo oggetto classe supporti anche [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) per la gestione delle licenze. Solo i fornitori interessati alle licenze devono supportare il meccanismo di gestione delle licenze di COM. In altre parole, poiché **IClassFactory2** è l'unico modo per ottenere le licenze a livello com, questa interfaccia è necessaria per l'oggetto classe per i controlli che vogliono avere la licenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 