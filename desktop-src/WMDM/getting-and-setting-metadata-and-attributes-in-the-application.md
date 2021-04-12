---
title: Accesso a metadati e attributi nell'app
description: Recupero e impostazione di metadati e attributi nell'applicazione
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media Gestione dispositivi, metadati
- Gestione dispositivi, metadati
- Guida per programmatori, metadati
- applicazioni desktop, metadati
- creazione di applicazioni Windows Media Gestione dispositivi, metadati
- metadata
- Windows Media Gestione dispositivi, attributi
- Gestione dispositivi, attributi
- Guida per programmatori, attributi
- applicazioni desktop, attributi
- creazione di applicazioni Windows Media Gestione dispositivi, attributi
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104335764"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Accesso a metadati e attributi nell'app

Una discussione generale sui metadati e sugli attributi è disponibile in [recupero e impostazione di metadati e attributi](getting-and-setting-metadata-and-attributes.md). In questa sezione vengono illustrate le chiamate al metodo dell'applicazione specifiche per recuperare o impostare i valori.

Le applicazioni possono recuperare gli attributi o i metadati relativi a un'archiviazione specifica chiamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata** recupera una raccolta completa di tutti i metadati associati a una risorsa di archiviazione e l'applicazione può quindi enumerare tutti i valori o richiedere valori specifici dalla raccolta. **GetSpecifiedMetadata** crea un oggetto di metadati per conto del chiamante. Il chiamante può richiedere un subset dei dati disponibili compilando il parametro *ppwszPropNames* con una matrice delle stringhe di proprietà Windows Media Gestione dispositivi desiderate e il conteggio di tale matrice. L'oggetto di metadati restituito verrà compilato con le proprietà che possono essere recuperate. Non è possibile recuperare le proprietà che non possono essere recuperate. I metadati vengono restituiti in base al massimo sforzo.

Un dispositivo può impostare attributi o metadati in un'archiviazione chiamando [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)o [**IWMDMStorage3::**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)SetAttribute. Si noti che non esiste alcuna garanzia che i valori impostati siano persistenti, perché possono essere archiviati in un archivio di file esterno non persistente, i valori potrebbero non essere supportati o, il dispositivo potrebbe non supportare le proprietà come scrivibili.

È anche possibile ottenere o impostare i metadati relativi a un dispositivo chiamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) o [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Alla fine delle [costanti dei metadati](metadata-constants.md)è presente una tabella separata di costanti dei metadati del dispositivo.

Esempi di utilizzo di questi metodi sono forniti nella documentazione di riferimento di ciascun metodo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Recupero e impostazione di metadati e attributi**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




