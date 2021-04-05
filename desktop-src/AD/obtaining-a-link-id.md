---
title: Ottenere un ID di collegamento
description: A partire da Windows Server 2003, non è più necessario richiedere un linkID da Microsoft; è disponibile un processo per la generazione automatica di un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Ottenere un ID di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117550"
---
# <a name="obtaining-a-link-id"></a>Ottenere un ID di collegamento

A partire da Windows Server 2003, non è più necessario richiedere un [**LinkId**](/windows/desktop/ADSchema/a-linkid) da Microsoft; è disponibile un processo per la generazione automatica di un **LinkId**. Il sistema genererà automaticamente un ID collegamento per un nuovo attributo collegato quando l'attributo **LinkId** dell'attributo viene impostato su 1.2.840.113556.1.2.50. Viene creato un collegamento indietro per questo collegamento in diretta impostando **LinkId** su [**attributeId**](/windows/desktop/ADSchema/a-attributeid) o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del collegamento in diretta. La cache dello schema deve essere ricaricata dopo aver creato il collegamento in diretta e prima di creare il collegamento indietro. In caso contrario, l'elemento **attributeId** o **ldapDisplayName** del collegamento diretto non verrà trovato quando viene creato il collegamento indietro. La cache dello schema viene ricaricata su richiesta, pochi minuti dopo che è stata apportata una modifica dello schema o quando il controller di dominio viene riavviato. Creare tutti i collegamenti in secondo piano, ricaricare la cache dello schema e quindi creare tutti i collegamenti indietro.

Ad esempio, quando sono stati creati i nuovi attributi **myForwardLinkAttr** e **myBackLinkAttr** e si desidera collegarli:

> [!Note]  
> Il OID in questo esempio è escogitato. Per istruzioni su come ottenere OID per i nuovi attributi, vedere [ottenere un identificatore di oggetto da Microsoft](obtaining-an-object-identifier-from-microsoft.md) .

 

1.  Impostare questi attributi sull'attributo che deve essere il collegamento in avanti:
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

 

 