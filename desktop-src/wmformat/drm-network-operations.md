---
title: Operazioni di rete DRM
description: Operazioni di rete DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK, operazioni di rete DRM
- Advanced Systems Format (ASF), operazioni di rete DRM
- ASF (Advanced Systems Format),Operazioni di rete DRM
- digital rights management (DRM), operazioni di rete
- DRM (Digital Rights Management),operazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f026ed972b88a1e6290bdd513012c2fab758da2c5b4b91a6a1162df5d258207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771751"
---
# <a name="drm-network-operations"></a>Operazioni di rete DRM

Diverse operazioni correlate a DRM richiedono che l'applicazione si connetta a un servizio in esecuzione in una rete. Queste operazioni includono l'individualizzazione, l'acquisizione delle licenze, la revoca delle licenze e il backup e il ripristino delle licenze.

Come per qualsiasi transazione di rete, l'applicazione deve prendere in considerazione una serie di difficoltà quando si includono funzionalità che richiedono operazioni di rete. L'applicazione deve tenere traccia dello stato dell'operazione in qualsiasi misura possibile per la funzionalità specifica, in genere gestendo i messaggi di stato. È consigliabile fornire all'utente commenti e suggerimenti sullo stato. Se un'operazione non riesce al primo tentativo, è consigliabile concedere all'utente la possibilità di riprovare. In molti casi, il primo tentativo ha difficoltà, ma un tentativo successivo viene completato senza errori.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




