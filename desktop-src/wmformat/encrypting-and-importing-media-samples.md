---
title: Esempi di crittografia e importazione di supporti
description: Esempi di crittografia e importazione di supporti
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows SDK formato multimediale,importazione DRM
- Windows MEDIA Format SDK, importazione
- Windows MEDIA Format SDK, esempi di crittografia di file multimediali
- digital rights management (DRM), importazione
- DRM (Digital Rights Management),importazione
- digital rights management (DRM), esempi di crittografia dei supporti
- DRM (Digital Rights Management),esempi di crittografia dei supporti
- API estese del client DRM, importazione
- API estese client, importazione
- API estese del client DRM, esempi di crittografia dei supporti
- API client estese, esempi di crittografia dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed604fc114feed6bd308b9a89c6bde6d6c96abeb9e88a7b9ace19d553de1596
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658841"
---
# <a name="encrypting-and-importing-media-samples"></a>Esempi di crittografia e importazione di supporti

Per ogni esempio di supporto crittografato con Windows Media DRM, è necessario generare un valore salt rigorosamente maggiore di quello precedente (aumento monotona). Usare il nuovo valore salt per creare una chiave di crittografia transitoria applicando l'algoritmo di crittografia SHA-1 al vettore di inizializzazione concatenato al valore salt.

Crittografare quindi l'esempio in base all'algoritmo RC4 usando la chiave transitoria generata. Prima che l'esempio venga passato all'SDK, l'applicazione deve associare il valore salt all'esempio impostando un attributo di estensione.

Ecco i passaggi per crittografare gli esempi di supporti:

1.  Chiamare il **metodo QueryInterface** dell'oggetto di esempio per ottenere l'interfaccia [**INSSBuffer3.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
2.  Incrementare il valore salt.
3.  Crittografare l'esempio usando un algoritmo di crittografia RC1. Per la crittografia si crea una chiave concatenando il vettore di inizializzazione e il valore salt.
4.  Fornire il valore salt all'SDK chiamando [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Importazione DRM**](drm-import.md)
</dt> <dt>

[**Esempio di crittografia di esempio per supporti**](media-sample-encryption-example.md)
</dt> </dl>

 

 




