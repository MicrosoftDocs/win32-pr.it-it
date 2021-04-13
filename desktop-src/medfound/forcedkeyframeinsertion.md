---
description: Inserimento fotogramma chiave forzata
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserimento fotogramma chiave forzata (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484076"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserimento fotogramma chiave forzata (Microsoft Media Foundation)

Quando si configura un oggetto codificatore video, è possibile impostare un intervallo massimo per i fotogrammi chiave nel contenuto codificato. Tuttavia, il codec inserisce i fotogrammi chiave nell'intervallo indicato dal contenuto; l'intervallo del fotogramma chiave non è costante. Per alcune applicazioni, la distanza del fotogramma chiave è molto importante. Ad esempio, un'applicazione di modifica video necessita di fotogrammi chiave nei percorsi logici di un editor, ad esempio le interruzioni di scena e le transizioni di tipo Shot.

L'inserimento di fotogrammi chiave forzata è una funzionalità che consente di richiedere la codifica di un frame di input come fotogramma chiave. Il codificatore tenterà di rispettare queste richieste, ma le impostazioni del buffer (velocità in bit e finestra del buffer) configurate per la sessione di codifica hanno sempre la precedenza.

Gli oggetti del codificatore video implementano l'inserimento di fotogrammi chiave forzata come risposta a un'estensione dell'unità dati associata all'esempio di input. Per ulteriori informazioni sulle estensioni dell'unità dati, vedere [Using Data Unit Extensions](usingdataunitextensions.md).

I dati dell'estensione per l'inserimento di fotogrammi chiave forzata sono identificati dal valore GUID seguente: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Le singole estensioni sono valori **bool** . Impostare il valore su **true** per indicare una richiesta del fotogramma chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle estensioni dell'unità dati](usingdataunitextensions.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



