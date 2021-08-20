---
title: Metadati
description: I metadati, ai fini di questo SDK, sono informazioni che descrivono un file ASF o il contenuto del file.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows MEDIA Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format),panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad8a687db3fc21c6d73ee43e4f6530fd6e2e504433699f4619ee3165c7af0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846446"
---
# <a name="metadata"></a>Metadati

I metadati, ai fini di questo SDK, sono informazioni che descrivono un file ASF o il contenuto del file. La sezione di intestazione di un file ASF contiene tutti i metadati associati a tale file. I singoli elementi di metadati in un file ASF sono detti attributi. Ogni attributo ha un nome e un valore. In questa documentazione vengono usate costanti globali per identificare gli attributi. Ad esempio, il titolo di un file ASF viene archiviato **\_ nell'attributo g wszWMTitle.**

Per gestire le esigenze più comuni dei metadati, in Windows Media Format SDK sono definiti diversi attributi. È anche possibile creare attributi personalizzati. È tuttavia necessario fare attenzione quando si assegnano nomi agli attributi personalizzati, perché altri sviluppatori di applicazioni possono usare gli stessi nomi e possono verificarsi conflitti.

Alcuni attributi vengono impostati dall'SDK e non possono essere modificati manualmente. Ad esempio, quando si indicizza un file ASF, l'SDK imposta l'attributo **\_ g wszWMSeekable** per mostrare che il file può ora essere letto da qualsiasi punto specificato.

Altri attributi sono puramente in informazioni e devono essere impostati manualmente. Ad esempio, se si vuole tenere traccia dell'autore di un file, è necessario impostare **g \_ wszWMAuthor**.

L Windows Media Format SDK fornisce il supporto per gli attributi che si applicano all'intero file e gli attributi che si applicano ai singoli flussi.

È possibile usare Windows Media Format SDK per modificare i metadati nei file MP3, anche se è consigliabile usare sempre attributi conformi a ID3 nei file MP3 per mantenere la compatibilità con altri programmi di manipolazione MP3.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Oggetto Metadata Editor**](metadata-editor-object.md)
</dt> <dt>

[**Funzionalità dei metadati**](metadata-features.md)
</dt> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




