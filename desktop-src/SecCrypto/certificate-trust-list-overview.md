---
description: Oltre ai certificati e agli elenchi di revoche di certificati (CRL), l'archivio certificati CryptoAPI supporta l'elenco certificati attendibili (CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Panoramica dell'elenco di certificati attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bdbd8b5fdfe4b2d81f3faddb052c16ecf32428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883841"
---
# <a name="certificate-trust-list-overview"></a>Panoramica dell'elenco di certificati attendibili

Oltre ai certificati e agli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL), l' [*archivio certificati*](../secgloss/c-gly.md) [*CryptoAPI*](../secgloss/c-gly.md) supporta l' [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL). Un CTL è un elenco predefinito di elementi firmati da un'entità attendibile. Un CTL è un elenco di [*hash*](../secgloss/h-gly.md) di certificati o un elenco di nomi di file. Tutti gli elementi nell'elenco vengono autenticati e approvati da un'entità di firma attendibile. Una struttura del [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) è simile alle strutture di contesto di certificati e CRL. Un contesto CTL può essere salvato in modo permanente nell'archivio certificati.

Un CTL CryptoAPI è un elenco di elementi firmati da un'entità attendibile. L'elenco di elementi può essere qualsiasi, ad esempio un elenco di hash di certificati, o un elenco di nomi di file. Nella maggior parte dei casi, un CTL è un elenco di contesti di certificati con hash. Tutti gli elementi nell'elenco vengono autenticati e approvati dall'entità di firma. L'uso principale di scopi consentiti consiste nel verificare i messaggi firmati, usando l'elenco di scopi consentiti come origine dei [*certificati radice*](../secgloss/r-gly.md)attendibili.

La struttura del [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) è simile alle strutture del contesto del certificato e del CRL. Tuttavia, a differenza delle strutture di contesto del certificato e del CRL, la struttura del **\_ contesto CTL** contiene un membro **hCryptMsg** . Questo handle viene aperto tramite una chiamata a una delle funzioni che restituiscono una struttura del **\_ contesto CTL** , rendendo possibile l'utilizzo delle funzioni di messaggio per verificare la firma del CTL. Questa verifica è necessaria per garantire che un elenco di scopi consentiti non sia un CTL fasullo immesso da un'entità non autorizzata.

Per le procedure per creare un CTL firmato e salvarlo in un archivio certificati, vedere [creazione, firma e archiviazione di un elenco](creating-signing-and-storing-a-ctl.md)di scopi consentiti. Vedere anche [Verifica di un CTL](verifying-a-ctl.md) e [Verifica dei messaggi firmati usando scopi consentiti](verifying-signed-messages-by-using-ctls.md) per le procedure di verifica dettagliate.

 

 
