---
description: Oggetto ContentInfo ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Oggetto ContentInfo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305525"
---
# <a name="asf-contentinfo-object"></a>Oggetto ContentInfo ASF

L'oggetto *CONTENTINFO* ASF archivia le informazioni dall'oggetto intestazione ASF di un file. Un'applicazione può usare l'oggetto ContentInfo per gli scopi seguenti:

-   Leggere l'oggetto intestazione per un file multimediale esistente. In questo caso, l'oggetto ContentInfo analizza l'oggetto Header e archivia le informazioni sul file delle caratteristiche. Media Foundation espone alcune di queste proprietà tramite attributi e interfacce. Queste sono descritte in [Media Foundation attributi per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md).
-   Scrivere le informazioni di intestazione e costruire un oggetto intestazione per un nuovo file.
-   Inizializzare altri oggetti ASF, ad esempio il [separatore ASF](asf-splitter.md), il [multiplexer](asf-multiplexer.md)ASF e l'indicizzatore ASF, durante la lettura o la scrittura di un file multimediale.

Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Creazione dell'oggetto ContentInfo

Per creare una nuova istanza dell'oggetto ContentInfo, chiamare la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) . Questo metodo restituisce un puntatore a un oggetto ContentInfo vuoto che deve essere inizializzato per funzionare con un file ASF specifico. A seconda che l'applicazione legga un file esistente o scriva un nuovo file ASF, deve chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) o [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per popolare l'oggetto vuoto.

Per ulteriori informazioni su queste chiamate al metodo, vedere gli argomenti seguenti:

-   [Lettura dell'oggetto intestazione ASF di un file esistente](reading-the-asf-header-object-of-an-existing-file.md)
-   [Recupero di informazioni da oggetti Header ASF](getting-information-from-asf-header-objects.md)
-   [Scrittura di un oggetto intestazione ASF per un nuovo file](writing-an-asf-header-object-for-a-new-file.md)
-   [Attributi di Media Foundation per oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



