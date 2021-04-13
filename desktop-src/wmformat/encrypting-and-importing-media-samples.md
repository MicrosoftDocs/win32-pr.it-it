---
title: Crittografia e importazione di esempi di supporti
description: Crittografia e importazione di esempi di supporti
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK, importazione DRM
- Windows Media Format SDK, importazione
- Windows Media Format SDK, crittografia degli esempi di supporti
- Digital Rights Management (DRM), importazione
- DRM (Digital Rights Management), importazione
- Digital Rights Management (DRM), crittografia degli esempi di supporti
- DRM (Digital Rights Management), crittografia degli esempi di supporti
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, crittografia degli esempi di supporti
- API estese del client, crittografia degli esempi di contenuti multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398567"
---
# <a name="encrypting-and-importing-media-samples"></a>Crittografia e importazione di esempi di supporti

Per ogni esempio di supporto crittografato con Windows Media DRM, è necessario generare un valore salt che è strettamente superiore rispetto a quello precedente (a incremento progressivo costante). Usare il nuovo valore salt per creare una chiave di crittografia transitoria applicando l'algoritmo di crittografia SHA-1 al vettore di inizializzazione concatenato con il valore salt.

Successivamente, crittografare l'esempio in base all'algoritmo RC4 usando la chiave transitoria generata. Prima che l'esempio venga passato all'SDK, l'applicazione deve associare il valore salt all'esempio impostando un attributo di estensione.

Ecco i passaggi per la crittografia degli esempi di supporti:

1.  Chiamare il metodo **QueryInterface** dell'oggetto di esempio per ottenere l'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .
2.  Incrementare il valore salt.
3.  Crittografare l'esempio usando un algoritmo di crittografia RC1. Per la crittografia si crea una chiave concatenando il vettore di inizializzazione e il valore salt.
4.  Specificare il valore salt per l'SDK chiamando [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Importazione DRM**](drm-import.md)
</dt> <dt>

[**Esempio di crittografia di esempio multimediale**](media-sample-encryption-example.md)
</dt> </dl>

 

 




