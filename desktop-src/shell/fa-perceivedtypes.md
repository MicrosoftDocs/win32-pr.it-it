---
description: Un tipo percepito è una categoria di tipi di file che consente di identificare il tipo di file in Windows (e le applicazioni) come immagine, audio, documento o altro tipo.
title: Tipi percepiti (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995277"
---
# <a name="perceived-types-the-windows-shell"></a>Tipi percepiti (shell di Windows)

Un tipo percepito è una categoria di tipi di file che consente di identificare il tipo di file in Windows (e le applicazioni) come immagine, audio, documento o altro tipo. I tipi percepiti vengono usati per diversi scopi, inclusa la determinazione del tipo di cartella, che viene quindi usato per impostare le impostazioni di visualizzazione predefinite. Ad esempio, viene assegnata una modalità di visualizzazione predefinita delle anteprime a una cartella piena di file di tipo immagine percepita.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sui tipi percepiti](#about-perceived-types)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-perceived-types"></a>Informazioni sui tipi percepiti

I tipi percepiti, definiti come valori PerceivedType, sono simili ai tipi di file, ad eccezione del fatto che fanno riferimento a grandi categorie di tipi di formato di file anziché a tipi di file specifici. Ad esempio, immagine, testo, audio e compresso sono tipi percepiti. Ai tipi di file (in genere i tipi di file pubblici) può essere assegnato un tipo percepito e deve essere sempre assegnato uno ogni volta che ne è presente uno appropriato. Ad esempio, i tipi di file di immagine. bmp,. png,. jpg e. gif sono anche di tipo immagine percepita.

I tipi percepiti predefiniti sono i seguenti:

-   Cartella
-   Testo
-   Immagine
-   Audio
-   Video
-   Compresso
-   Documento
-   Sistema
-   Applicazione
-   Gamemedia
-   Contatti

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni su come registrare i tipi percepiti, vedere [registrazione dell'applicazione](app-registration.md).
-   Per un elenco di tipi percepiti predefiniti, vedere l'enumerazione [**percepita**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Per recuperare il tipo percepito di un file in base all'estensione del nome file, vedere la funzione [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 



