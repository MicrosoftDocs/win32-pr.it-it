---
description: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee50adc4e3f411bca9679672b88680ab3064bc91d828e2897ae1f94e40f9f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355211"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Scrittura di un oggetto intestazione ASF per un nuovo file

L'oggetto ContentInfo di ASF archivia le informazioni sull'oggetto intestazione ASF per un file. Quando viene creato o modificato un file ASF, è necessario generare l'oggetto Intestazione. A tale scopo, l'applicazione deve fornire il profilo di codifica del contenuto all'oggetto ContentInfo in modo che conosca le caratteristiche del file multimediale da creare.

Per scrivere un nuovo file, è possibile usare l'oggetto ContentInfo per:

-   Raccogliere le informazioni di intestazione dall'oggetto profilo del file da creare.
-   Popolare vari oggetti intestazione nella libreria ASF gestiti internamente da Media Foundation,
-   Inizializzare [asf Multiplexer per](asf-multiplexer.md) la generazione di pacchetti di dati ASF e
-   Costruire l'oggetto Header di primo livello in formato binario che può essere scritto in un file.

Per informazioni sui profili, vedere [Profilo ASF.](asf-profile.md)

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                                                              | Descrizione                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Descrive il metodo [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) che inizializza l'oggetto ContentInfo con le informazioni di intestazione archiviate in un oggetto profilo. |
| [Impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Informazioni sulle varie proprietà di configurazione che devono essere impostate nell'oggetto ContentInfo.                                                                                         |
| [Generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md)                                       | Come generare un buffer multimediale, che contiene l'oggetto intestazione ASF effettivo del nuovo file, dall'oggetto ContentInfo.                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo di ASF](asf-contentinfo-object.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> <dt>

Struttura del file ASF
</dt> </dl>

 

 



