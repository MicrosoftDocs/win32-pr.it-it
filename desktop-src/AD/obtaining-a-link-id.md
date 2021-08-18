---
title: Recupero di un ID collegamento
description: A partire Windows Server 2003, non è più necessario richiedere un linkID a Microsoft. è disponibile un processo per la generazione automatica di un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Recupero di un ID collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1800448e8cc665e0a28a88800a592e33d7b6ee5a766743d8a681a121c5ad02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025559"
---
# <a name="obtaining-a-link-id"></a>Recupero di un ID collegamento

A partire Windows Server 2003, non è più necessario richiedere un [**linkID**](/windows/desktop/ADSchema/a-linkid) a Microsoft. è disponibile un processo per la generazione automatica di **un linkID**. Il sistema genererà automaticamente un ID collegamento per un nuovo attributo collegato quando l'attributo **linkID** dell'attributo è impostato su 1.2.840.113556.1.2.50. Un collegamento indietro per questo collegamento in avanti viene creato impostando **linkID** su [**attributeID**](/windows/desktop/ADSchema/a-attributeid) o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del collegamento in avanti. La cache dello schema deve essere ricaricata dopo aver creato il collegamento in avanti e prima di creare il collegamento indietro. In caso contrario, **l'attributo AttributeId** o **ldapDisplayName** del collegamento di inoltro non verrà trovato quando viene creato il collegamento indietro. La cache dello schema viene ricaricata su richiesta, pochi minuti dopo la modifica dello schema o al riavvio del controller di dominio. Creare tutti i collegamenti in avanti, ricaricare la cache dello schema e quindi creare tutti i collegamenti indietro.

Ad esempio, dopo aver creato i nuovi attributi **myForwardLinkAttr** e **myBackLinkAttr** e si vuole collegarli:

> [!Note]  
> Gli OID in questo esempio sono contrived. Per istruzioni su come ottenere gli OID per i nuovi attributi, vedere Ottenere un identificatore di oggetto da [Microsoft.](obtaining-an-object-identifier-from-microsoft.md)

 

1.  Impostare questi attributi sull'attributo che deve essere il collegamento di inoltro:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Ricaricare lo schema.
3.  Impostare questi attributi sull'attributo che deve essere il collegamento indietro:
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi collegati](linked-attributes.md)
</dt> <dt>

[Come estendere lo schema](how-to-extend-the-schema.md)
</dt> </dl>

 

 