---
title: Enumerazione delle licenze nell'archivio licenze locale
description: Enumerazione delle licenze nell'archivio licenze locale
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, enumerazione delle licenze
- Windows Media Format SDK, licenze
- Windows Media Format SDK, archivio licenze locale
- DRM (Digital Rights Management), enumerazione delle licenze
- DRM (Digital Rights Management),enumerazione delle licenze
- digital rights management (DRM), licenze
- DRM (Digital Rights Management),licenze
- digital rights management (DRM), archivio licenze locale
- DRM (Digital Rights Management),archivio licenze locale
- API estese del client DRM, enumerazione delle licenze
- API estese client, enumerazione delle licenze
- API estese del client DRM, licenze
- API client estese, licenze
- API estese del client DRM, archivio licenze locale
- API client estese, archivio licenze locale
- licenze, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27913a5a35ce9af1f5a4d6fa3cbae808bc2abe89afd5edb05aa927fe4c39227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848197"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumerazione delle licenze nell'archivio licenze locale

L'enumerazione è un processo che consente di ottenere informazioni sulle licenze nell'archivio licenze locale, passandole una alla volta. È possibile creare un'enumerazione delle licenze chiamando [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

Il motivo più comune per enumerare le licenze nello Store è trovare una licenza specifica per la decrittografia di alcuni contenuti.

[**L'interfaccia IWMDRMLicense**](iwmdrmlicense.md) funge sia da portale per i risultati delle singole licenze che come enumeratore. Quando viene creata l'enumerazione delle licenze, la prima licenza nell'elenco viene caricata **nell'interfaccia IWMDRMLicense.** La maggior parte dei metodi **di IWMDRMLicense** consente di ottenere informazioni sulla licenza o di creare oggetti per crittografare o decrittografare il contenuto in base alla licenza. Esistono tuttavia due metodi che controllano l'enumerazione: [**GetNext**](iwmdrmlicense-getnext.md) [**e ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** carica la licenza successiva nell'elenco nell'interfaccia . **ResetEnumeration** restituisce l'enumerazione allo stato in cui si era al momento della creazione. Quando l'enumerazione viene reimpostata, la prima licenza nell'elenco viene caricata nuovamente **nell'interfaccia IWMDRMLicense.**

Dopo aver raggiunto l'ultima licenza nell'elenco, la chiamata successiva a **GetNext** restituisce ERROR \_ NO MORE \_ \_ ITEMS.

Se l'applicazione esegue un'azione con il contenuto coperto da DRM, è necessario controllare le licenze nell'archivio licenze locale per i diritti e per altri fattori limitanti, ad esempio i livelli di protezione dell'output (OPL).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di informazioni dalle licenze nell'archivio licenze locale**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




