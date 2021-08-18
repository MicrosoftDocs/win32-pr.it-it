---
description: Inserimento forzato del fotogramma chiave
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserimento forzato di fotogrammi chiave (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9790a40c7fc6d2248377003005bbff7ad56b54208e1d20814d5c8150223198ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466141"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserimento forzato di fotogrammi chiave (Microsoft Media Foundation)

Quando si configura un oggetto codificatore video, è possibile impostare un intervallo massimo per i fotogrammi chiave nel contenuto codificato. Tuttavia, il codec inserirà fotogrammi chiave all'interno di tale intervallo come determinato dal contenuto; L'intervallo del fotogramma chiave non è costante. Per alcune applicazioni, la distanza del fotogramma chiave è molto importante. Ad esempio, un'applicazione di modifica video richiede fotogrammi chiave in posizioni logiche a un editor, ad esempio in caso di interruzioni di scena e transizioni di ripresa.

L'inserimento forzato di fotogrammi chiave è una funzionalità che consente di richiedere la codifica di un fotogramma di input come fotogramma chiave. Il codificatore tenterà di rispettare queste richieste, ma le impostazioni del buffer (velocità in bit e finestra del buffer) configurate per la sessione di codifica hanno sempre la precedenza.

Gli oggetti codificatore video implementano l'inserimento forzato di fotogrammi chiave come risposta a un'estensione unità dati collegata all'esempio di input. Per altre informazioni sulle estensioni di unità dati, vedere [Uso delle estensioni unità dati](usingdataunitextensions.md).

I dati di estensione per l'inserimento forzato di fotogrammi chiave sono identificati dal valore GUID **seguente: F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Le singole estensioni sono **valori BOOL.** Impostare il valore su **TRUE per** indicare una richiesta di fotogramma chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle estensioni per unità dati](usingdataunitextensions.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



