---
title: Protezione DRM e distribuzione delle licenze di contenuti
description: Protezione DRM e distribuzione delle licenze di contenuti
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, protezione del contenuto DRM
- Windows Media Format SDK, licenze DRM
- ASF (Advanced Systems Format), protezione del contenuto DRM
- ASF (Advanced Systems Format), protezione del contenuto DRM
- ASF (Advanced Systems Format), distribuzione di licenze DRM
- ASF (Advanced Systems Format), distribuzione di licenze DRM
- Digital Rights Management (DRM), protezione del contenuto
- DRM (Digital Rights Management), protezione del contenuto
- Digital Rights Management (DRM), distribuzione di licenze
- DRM (Digital Rights Management), distribuzione di licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332564"
---
# <a name="drm-protection-and-content-license-distribution"></a>Protezione DRM e distribuzione delle licenze di contenuti

Sul lato della creazione, Digital Rights Management tecnologia implica due processi principali: (1) proteggere il contenuto e (2) fornire le licenze per il contenuto. La protezione di un file comporta essenzialmente la crittografia del contenuto e l'inclusione di un URL nell'intestazione del file che specifica dove è possibile ottenere una licenza per il contenuto. Per proteggere i file con e quindi distribuire i file in altri computer o dispositivi, è possibile usare Windows Media Format SDK o Windows Media Rights Manager SDK per proteggere il file. Per gli scenari di DRM Live, è necessario usare Windows Media Format SDK per proteggere il contenuto mentre viene codificato.

Per creare ed emettere licenze per il contenuto protetto, è possibile creare una soluzione personalizzata usando gli oggetti di Windows Media Rights Manager SDK oppure è possibile usare un servizio eseguito da terze parti.

Indipendentemente dal metodo utilizzato, i file protetti creati conterranno, nell'oggetto intestazione DRM, un URL che indica alle applicazioni client dove ottenere una licenza per il contenuto.

> [!Note]  
> Windows Media Format SDK non fornisce supporto per la creazione o l'emissione di licenze.

 

Sul lato riproduzione, un'applicazione abilitata per DRM deve essere in grado di ottenere le licenze per il contenuto protetto, di decrittografare il contenuto usando la chiave contenuta nella licenza e di applicare le restrizioni di licenza, ad esempio il numero di volte in cui un file può essere riprodotto o se il file può essere copiato in un altro dispositivo. Windows Media Format SDK fornisce tutto il supporto necessario per creare un'applicazione di riproduzione DRM completamente abilitata.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




