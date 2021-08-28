---
title: Esportazione di contenuto compresso
description: Esportazione di contenuto compresso
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows MEDIA Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows Media Format SDK, contenuto compresso
- digital rights management (DRM), esportazione
- DRM (Digital Rights Management),esportazione
- digital rights management (DRM), contenuto compresso
- DRM (Digital Rights Management),contenuto compresso
- API estese del client DRM, contenuto compresso
- API client estese, contenuto compresso
- API estese del client DRM, esportazione
- API client estese, esportazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055501"
---
# <a name="exporting-compressed-content"></a>Esportazione di contenuto compresso

Questa sezione descrive l'esportazione Windows file multimediali protetti da Media DRM in un file Windows Media in cui l'applicazione riceve dati multimediali digitali compressi. A tale scopo, l'applicazione deve eseguire la decrittografia inline di tutti Windows payload crittografati con Media DRM in un file ASF.

> [!Note]  
> Una libreria di analisi ASF viene fornita all'utente come parte del contratto Windows'esportazione di Media DRM.

 

I passaggi principali per l'esportazione di contenuto compresso sono:

1.  Eseguire l'individualizzazione DRM, se necessario.
2.  Verificare che lo schema di protezione del contenuto di destinazione sia consentito in modo esplicito.
3.  Creare un oggetto di decrittografia per decrittografare ogni payload asf.
4.  Il sistema DRM transcrittografa ogni payload ASF da Windows Media DRM in RC4 prima di passarlo all'applicazione.

Se l'applicazione modifica le dimensioni di un payload ASF durante la transcrittografia, è necessario anche rimultiplexare il file ASF.

Passare alla libreria stub un certificato Windows'applicazione di esportazione DRM multimediale. Il certificato viene verificato e, se valido, il sistema DRM genera un vettore di inizializzazione e lo crittografa usando RSA OAEP.

-   Viene creata una chiave di sessione RC4 per ogni payload concatenando il vettore di inizializzazione e un valore salt. Si specifica il valore salt all'API di decrittografia ed è necessario incrementarlo di un valore intero positivo diverso da zero per ogni payload.

Verrà fornito uno strumento da Microsoft come parte del contratto di esportazione di Windows Media DRM che consentirà di generare la propria coppia di chiavi RSA pubblica/privata. Si invierà la chiave pubblica a Microsoft, dove Microsoft la incorporerà in un certificato dell'applicazione Windows Media DRM firmato e la restituirà.

Ogni payload, dopo essere stato decrittografato usando la chiave di decrittografia RC4, deve essere immediatamente crittografato nel CPS di output. Esistono altre restrizioni per la gestione dei payload non crittografati descritte nelle regole di affidabilità e conformità, che accompagnano il contratto di esportazione Windows Media DRM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Decrittografia e ricrittografia del payload ASF**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Esportazione DRM**](drm-export.md)
</dt> <dt>

[**Esecuzione della individualizzazione DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Verifica e inizializzazione**](verification-and-initialization.md)
</dt> </dl>

 

 




