---
description: Oltre ai certificati e agli elenchi di revoche di certificati (CRL), l'archivio certificati CryptoAPI supporta l'elenco di certificati attendibili (CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Panoramica dell'elenco di certificati attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771107"
---
# <a name="certificate-trust-list-overview"></a>Panoramica dell'elenco di certificati attendibili

Oltre ai certificati e agli elenchi di [*revoche*](../secgloss/c-gly.md) di certificati (CRL), l'archivio certificati [*CryptoAPI*](../secgloss/c-gly.md) [*supporta*](../secgloss/c-gly.md) l'elenco di certificati attendibili [](../secgloss/c-gly.md) (CTL). Un CTL è un elenco predefinito di elementi firmati da un'entità attendibile. Un CTL è un elenco [*di hash di*](../secgloss/h-gly.md) certificati o un elenco di nomi di file. Tutti gli elementi nell'elenco vengono autenticati e approvati da un'entità di firma attendibile. Una [**struttura CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) è simile alle strutture di contesto del certificato e CRL. Un contesto CTL può essere salvato in modo permanente nell'archivio certificati.

Un CTL CryptoAPI è un elenco di elementi firmati da un'entità attendibile. L'elenco di elementi può essere qualsiasi elemento, ad esempio un elenco di hash di certificati o un elenco di nomi di file. Nella maggior parte dei casi, un CTL è un elenco di contesti di certificato con hash. Tutti gli elementi nell'elenco vengono autenticati e approvati dall'entità di firma. L'uso principale dei CTL è la verifica dei messaggi firmati, usando l'elenco CTL come origine di certificati [*radice attendibili.*](../secgloss/r-gly.md)

La [**struttura CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) è simile alle strutture di contesto del certificato e CRL. Tuttavia, a differenza delle strutture di contesto del certificato e CRL, la struttura **CTL \_ CONTEXT** contiene un membro **hCryptMsg.** Questo handle viene aperto da una chiamata a una delle funzioni che restituiscono una struttura **CONTEXT CTL, \_** rendendo possibile usare le funzioni di messaggio per verificare la firma del CTL. Questa verifica è necessaria per garantire che un CTL non sia un CTL falso piantato da un'entità non autorizzata.

Per le procedure per creare un CTL firmato e salvarlo in un archivio certificati, vedere Creazione, firma e archiviazione di [un CTL.](creating-signing-and-storing-a-ctl.md) Vedere anche [Verifying a CTL](verifying-a-ctl.md) and Verifying Signed Messages By Using CTLs (Verifica di un CTL) e Verifying Signed Messages By Using CTLs (Verifica di un CTL) e [Verifying Signed Messages By Using CTLs](verifying-signed-messages-by-using-ctls.md) (Verifica dei messaggi firmati tramite CTL) per le procedure di verifica dettagliate.

 

 
