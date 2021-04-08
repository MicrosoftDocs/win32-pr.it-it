---
title: Esportazione di contenuto compresso
description: Esportazione di contenuto compresso
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows Media Format SDK, contenuto compresso
- Digital Rights Management (DRM), esportazione
- DRM (Digital Rights Management), esportazione
- Digital Rights Management (DRM), contenuto compresso
- DRM (Digital Rights Management), contenuto compresso
- API estese del client DRM, contenuto compresso
- API estese client, contenuto compresso
- API estese del client DRM, esportazione
- API estese client, esportazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855918"
---
# <a name="exporting-compressed-content"></a>Esportazione di contenuto compresso

In questa sezione viene descritta l'esportazione di supporti DRM protetti con Windows Media in un file Windows Media in cui l'applicazione riceve dati multimediali digitali compressi. A tale scopo, l'applicazione deve eseguire la decrittografia inline di tutti i payload crittografati DRM di Windows Media in un file ASF.

> [!Note]  
> Una libreria di analisi ASF viene fornita all'utente come parte del contratto di esportazione DRM di Windows Media.

 

I passaggi principali necessari per esportare il contenuto compresso sono:

1.  Se necessario, eseguire l'individualizzazione DRM.
2.  Verificare che lo schema di protezione del contenuto di destinazione sia consentito in modo esplicito.
3.  Creare un oggetto di decrittografia per decrittografare ogni payload ASF.
4.  Il sistema DRM transcrypta ogni payload ASF da Windows Media DRM in RC4 prima di passarlo all'applicazione.

Se l'applicazione modifica la dimensione di un payload ASF durante la transcryption, è necessario rimultiplexare anche il file ASF.

Passare alla libreria stub un certificato dell'applicazione Windows Media DRM Export. Il certificato viene verificato e, se è valido, il sistema DRM genera un vettore di inizializzazione e lo crittografa usando RSA OAEP.

-   Viene creata una chiave di sessione RC4 per ogni payload concatenando il vettore di inizializzazione e un valore salt. Il valore salt viene fornito all'API di decrittografia ed è necessario incrementarlo per un valore integer positivo diverso da zero per ogni payload.

Verrà fornito uno strumento di Microsoft nell'ambito del contratto di esportazione DRM di Windows Media che consente di generare una coppia di chiavi pubblica/privata RSA personalizzata. Si invierà la chiave pubblica a Microsoft, in cui Microsoft la inserirà in un certificato dell'applicazione Windows Media DRM firmato e lo restituirà.

Ogni payload, dopo essere stato decrittografato con la chiave di decrittografia RC4, deve essere immediatamente crittografato nel CPS di output. Esistono altre restrizioni sulla gestione dei payload non crittografati descritti nelle regole di affidabilità e conformità, che accompagnano il contratto di esportazione di Windows Media DRM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Decrittografia e ricrittografia del payload ASF**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Esportazione DRM**](drm-export.md)
</dt> <dt>

[**Esecuzione dell'individualizzazione DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Verifica e inizializzazione**](verification-and-initialization.md)
</dt> </dl>

 

 




