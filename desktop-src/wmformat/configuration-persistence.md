---
title: Persistenza della configurazione
description: Persistenza della configurazione
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistenza
- Windows Media Format SDK, persistenza della configurazione
- ASF (Advanced Systems Format), persistenza
- ASF (formato avanzato dei sistemi), persistenza
- ASF (Advanced Systems Format), persistenza della configurazione
- ASF (formato avanzato dei sistemi), persistenza della configurazione
- persistenza della configurazione
- persistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398630"
---
# <a name="configuration-persistence"></a>Persistenza della configurazione

Nessuna delle proprietà abilitate per la scrittura descritte in questa documentazione viene salvata da Windows Media SDK. Ogni applicazione che usa l'SDK deve fornire le proprie procedure di persistenza, se necessario, e richiamare il metodo set appropriato su ogni istanza dell'SDK. In questo modo, le modifiche di configurazione apportate da un'applicazione non influiscono su un'altra applicazione. Ad esempio, la modifica del tempo di buffering in un lettore non influisce su un altro lettore.

L'unica eccezione a questa regola è rappresentata dalle informazioni sulle credenziali. Se l'applicazione indica, nell'output restituito dalla chiamata a **AcquireCredentials** , che le informazioni sull'ID utente e sulla password devono essere rese permanente, l'SDK Salva queste informazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> <dt>

[**Interfaccia IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




