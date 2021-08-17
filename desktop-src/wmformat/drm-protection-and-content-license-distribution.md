---
title: Protezione DRM e distribuzione delle licenze per i contenuti
description: Protezione DRM e distribuzione delle licenze per i contenuti
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, protezione del contenuto DRM
- Windows Media Format SDK, licenze DRM
- Advanced Systems Format (ASF), protezione del contenuto DRM
- ASF (Advanced Systems Format),Protezione del contenuto DRM
- Advanced Systems Format (ASF), distribuzione delle licenze DRM
- ASF (Advanced Systems Format),distribuzione delle licenze DRM
- digital rights management (DRM), protezione del contenuto
- DRM (Digital Rights Management),protezione del contenuto
- digital rights management (DRM), distribuzione delle licenze
- DRM (Digital Rights Management),distribuzione delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704315"
---
# <a name="drm-protection-and-content-license-distribution"></a>Protezione DRM e distribuzione delle licenze per i contenuti

Sul lato della creazione, la tecnologia di gestione dei diritti digitali prevede due processi principali: (1) proteggere il contenuto e (2) fornire le licenze per il contenuto. La protezione di un file implica fondamentalmente la crittografia del contenuto e l'inclusione di un URL nell'intestazione del file che specifica dove è possibile ottenere una licenza per il contenuto. Se si desidera proteggere i file con e quindi distribuirvi ad altri computer o dispositivi, è possibile usare Windows Media Format SDK o Windows Media Rights Manager SDK per proteggere il file. Per gli scenari DRM live, è necessario usare Windows Media Format SDK per proteggere il contenuto durante la codifica.

Per creare ed emettere licenze per il contenuto protetto, è possibile creare una soluzione personalizzata usando gli oggetti di Windows Media Rights Manager SDK oppure è possibile usare un servizio eseguito da terze parti.

Indipendentemente dal metodo in uso, i file protetti creati conterranno, nell'oggetto intestazione DRM, un URL che indica alle applicazioni client dove ottenere una licenza per il contenuto.

> [!Note]  
> L Windows Media Format SDK non fornisce supporto per la creazione o il rilascio di licenze.

 

Sul lato della riproduzione, un'applicazione abilitata per DRM deve essere in grado di ottenere licenze per il contenuto protetto, decrittografare il contenuto usando la chiave contenuta nella licenza e applicare le restrizioni di licenza, ad esempio il numero di volte in cui un file può essere riprodotto o se il file può essere copiato in un altro dispositivo. L Windows Media Format SDK offre tutto il supporto necessario per creare un'applicazione di riproduzione DRM completamente abilitata.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




