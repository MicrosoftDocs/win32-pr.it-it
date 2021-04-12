---
title: Metadati
description: Ai fini di questo SDK, i metadati sono informazioni che descrivono un file ASF o il contenuto del file.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format), panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332295"
---
# <a name="metadata"></a>Metadati

Ai fini di questo SDK, i metadati sono informazioni che descrivono un file ASF o il contenuto del file. La sezione di intestazione di un file ASF contiene tutti i metadati associati a tale file. Singoli elementi di metadati in un file ASF sono denominati attributi. Ogni attributo ha un nome e un valore. In questa documentazione vengono usate le costanti globali per identificare gli attributi. Ad esempio, il titolo di un file ASF viene archiviato nell'attributo **g \_ wszWMTitle** .

In Windows Media Format SDK sono definiti diversi attributi che consentono di gestire le esigenze più comuni dei metadati. Inoltre, è possibile creare attributi personalizzati. È necessario prestare attenzione quando si denominano gli attributi personalizzati, tuttavia, poiché altri sviluppatori di applicazioni possono utilizzare gli stessi nomi e possono verificarsi conflitti.

Alcuni attributi vengono impostati dall'SDK e non possono essere modificati manualmente. Ad esempio, quando si indicizza un file ASF, l'SDK imposta l'attributo **g \_ wszWMSeekable** per indicare che è ora possibile leggere il file da un punto specificato.

Gli altri attributi sono puramente informativi e devono essere impostati manualmente. Ad esempio, se si vuole tenere traccia dell'autore di un file, è necessario impostare **g \_ wszWMAuthor**.

Windows Media Format SDK fornisce il supporto per gli attributi applicabili all'intero file e gli attributi che si applicano ai singoli flussi.

È possibile utilizzare Windows Media Format SDK per modificare i metadati nei file MP3, anche se è consigliabile utilizzare sempre gli attributi conformi a ID3 nei file MP3 per mantenere la compatibilità con altri programmi di manipolazione MP3.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Oggetto Metadata Editor**](metadata-editor-object.md)
</dt> <dt>

[**Funzionalità dei metadati**](metadata-features.md)
</dt> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




