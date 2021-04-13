---
title: Operazioni di rete DRM
description: Operazioni di rete DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK, operazioni di rete DRM
- ASF (Advanced Systems Format), operazioni di rete DRM
- ASF (Advanced Systems Format), operazioni di rete DRM
- Digital Rights Management (DRM), operazioni di rete
- DRM (Digital Rights Management), operazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328692"
---
# <a name="drm-network-operations"></a>Operazioni di rete DRM

Per diverse operazioni relative a DRM è necessario che l'applicazione si connetta a un servizio in esecuzione in una rete. Queste operazioni includono l'individualizzazione, l'acquisizione di licenze, la revoca delle licenze e il backup e il ripristino delle licenze.

Come per qualsiasi transazione di rete, l'applicazione deve tenere conto di una serie di difficoltà quando si includono funzionalità che richiedono operazioni di rete. L'applicazione deve tenere traccia dello stato dell'operazione in base a qualsiasi extent possibile per la funzionalità specifica, in genere gestendo i messaggi di stato. È necessario fornire un feedback all'utente sullo stato. Se un'operazione non riesce al primo tentativo, è necessario concedere all'utente la possibilità di riprovare. In molti casi, il primo tentativo rileva difficoltà, ma un tentativo successivo viene completato senza errori.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




