---
description: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Scrittura di un oggetto intestazione ASF per un nuovo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317303"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Scrittura di un oggetto intestazione ASF per un nuovo file

Il valore ASF oggetto consente di archiviare le informazioni sull'oggetto intestazione ASF per un file. Quando si crea o si modifica un file ASF, è necessario generare l'oggetto intestazione. A tale scopo, l'applicazione deve fornire il profilo di codifica del contenuto all'oggetto ContentInfo in modo che conosca le caratteristiche del file multimediale da creare.

Per scrivere un nuovo file, è possibile usare l'oggetto ContentInfo per:

-   Raccogliere le informazioni di intestazione dall'oggetto profilo del file da creare.
-   Popola i vari oggetti intestazione nella libreria ASF gestita internamente da Media Foundation,
-   Inizializzare [ASF Multiplexer](asf-multiplexer.md) per la generazione di pacchetti di dati ASF e
-   Costruisce l'oggetto intestazione di primo livello in formato binario che può essere scritto in un file.

Per informazioni sui profili, vedere [profilo ASF](asf-profile.md).

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                                                              | Descrizione                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Viene descritto il metodo [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) che Inizializza l'oggetto ContentInfo con le informazioni di intestazione archiviate in un oggetto profilo. |
| [Impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Informazioni sulle varie proprietà di configurazione che devono essere impostate nell'oggetto ContentInfo.                                                                                         |
| [Generazione di un nuovo oggetto intestazione ASF](generating-a-new-asf-header-object.md)                                       | Come generare un buffer multimediale, che contiene l'oggetto intestazione ASF effettivo del nuovo file, dall'oggetto ContentInfo.                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo ASF](asf-contentinfo-object.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

Struttura di file ASF
</dt> </dl>

 

 



