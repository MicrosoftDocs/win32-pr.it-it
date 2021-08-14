---
title: Persistenza della configurazione
description: Persistenza della configurazione
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows MEDIA Format SDK, persistenza
- Windows MEDIA Format SDK, persistenza della configurazione
- Advanced Systems Format (ASF), persistenza
- ASF (Advanced Systems Format),persistenza
- Advanced Systems Format (ASF), persistenza della configurazione
- ASF (Advanced Systems Format),persistenza della configurazione
- persistenza della configurazione
- persistence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b5b2442779fb709299f42e0194317aadaf54a51cd4946e61adf7a90a50957d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434358"
---
# <a name="configuration-persistence"></a>Persistenza della configurazione

Nessuna delle proprietà abilitate per la scrittura descritta in questa documentazione viene salvata da Windows Media SDK. Ogni applicazione che usa l'SDK deve fornire le proprie procedure di persistenza in base alle esigenze e richiamare il metodo set appropriato in ogni istanza dell'SDK. In questo modo, le modifiche di configurazione apportate da un'applicazione non influiscono su un'altra applicazione. Ad esempio, la modifica del tempo di memorizzazione nel buffer in un lettore non influisce su un altro giocatore.

L'unica eccezione a questa regola è per le informazioni sulle credenziali. Se l'applicazione indica, in risposta alla chiamata **AcquireCredentials,** che le informazioni sull'ID utente e sulla password devono essere rese persistenti, l'SDK salva queste informazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> <dt>

[**Interfaccia IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




