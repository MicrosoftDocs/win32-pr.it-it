---
description: Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema usati per archiviare le informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo.
title: Matrici di associazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128887"
---
# <a name="association-arrays"></a>Matrici di associazione

Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema usati per archiviare le informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo. La shell USA matrici di associazione per eseguire una query su un set predefinito di percorsi del registro di sistema che potrebbero contenere informazioni su un elemento della shell.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulle matrici di associazione](#about-association-arrays)
-   [Esecuzione di query su matrici di associazione](#querying-association-arrays)
-   [Utilizzo di matrici di associazione per una determinata origine dati della shell](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Matrici di associazioni di origini dati della shell](#shell-data-source-association-arrays)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-association-arrays"></a>Informazioni sulle matrici di associazione

Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema che contengono informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, ad esempio l'icona e il nome visualizzato del tipo. Queste informazioni sul tipo di elemento possono essere registrate a diversi livelli di specificità. È ad esempio possibile registrare un verbo che sarà visualizzato solo per un tipo di file specifico, ad esempio. jpg, oppure per tutti gli elementi con lo stesso sistema. Kind (ad esempio, System. Kind = immagine) o per tutti gli elementi.

La shell USA matrici di associazione per eseguire una query su un set predefinito di percorsi del registro di sistema che potrebbero potenzialmente contenere informazioni sull'elemento. Le API di Association array possono essere usate per recuperare dalla sottochiave del registro di sistema un singolo valore che contiene le informazioni richieste, con tale valore proveniente dalla prima voce della matrice che lo fornisce. Il valore predefinito dell'icona, ad esempio, viene recuperato in questo modo. La matrice di associazioni può essere utilizzata anche per recuperare un set di valori archiviati nelle sottochiavi del registro di sistema. Ad esempio, l'elenco dei verbi viene compilato da quei verbi registrati in tutte le sottochiavi.

Quando la shell esegue una query su un set predefinito di percorsi del registro di sistema per ottenere informazioni su un elemento della shell, inserisce i percorsi del registro di sistema in una matrice in ordine dalla posizione più specifica alla più generale.

Poiché le matrici di associazione sono elenchi ordinati, forniscono agli sviluppatori di applicazioni un meccanismo per l'aggiunta di informazioni al registro di sistema che verranno restituite per un tipo specifico di elemento. Analogamente, gli array di associazioni consentono agli sviluppatori di applicazioni di aggiungere informazioni al registro di sistema per un gruppo specifico di elementi quando tali elementi sono registrati in una posizione più generale. Questa logica informa la decisione sulla posizione più appropriata nel registro di sistema per archiviare le informazioni sugli elementi della shell.

In un sistema Windows predefinito, un file con estensione jpg presenta la seguente matrice di associazioni:

-   **HKEY \_ Jpgfile \_ radice classi** \\ 
-   **HKEY \_ Classi \_ radice** \\ **SystemFileAssociations** \\ **. jpg**
-   **HKEY \_ Immagine \_ radice classi** \\ 
-   **HKEY \_ \_radice classi** \\ * *\** _
-   _ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects**

Per informazioni sulla registrazione di matrici di associazione, vedere [registrazione dell'applicazione](app-registration.md).

## <a name="querying-association-arrays"></a>Esecuzione di query su matrici di associazione

Sono disponibili API shell per recuperare informazioni da un intervallo di sottochiavi del registro di sistema, dalla sottochiave del registro di sistema più specifica a un superset delle informazioni in tutte le sottochiavi del registro di sistema.

L'uso più comune di una matrice di associazioni consiste nell'eseguire una query per ottenere un singolo valore restituito dalla Shell dall'elemento più specifico della matrice con le informazioni richieste. Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



Le API seguenti possono essere utilizzate per eseguire una query su una matrice di associazioni o per costruire un oggetto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) della matrice di associazione su cui è possibile eseguire una query:

-   [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prima di Windows Vista)
-   [**AssocCreateForClasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>Utilizzo di matrici di associazione per una determinata origine dati della shell

Ogni origine dati della shell definisce la matrice di associazioni per i relativi elementi. La definizione di una matrice di associazioni è in genere una funzione del tipo di elemento. Gli implementatori di origini dati della shell devono definire e documentare le matrici di associazione per consentire alle applicazioni di estendere il comportamento di tali tipi, ad esempio per la registrazione di verbi o altre informazioni. Le applicazioni possono estendere il comportamento degli elementi in base all'aggiunta di dati alle sottochiavi di matrice di associazione, ad esempio l'aggiunta di verbi per gli elementi.

L'origine dati file system compila una matrice di associazioni per i file in base alle sottochiavi del registro di sistema e ai ProgID speciali seguenti:

-   Se il file ha un ProgID registrato, viene usato il ProgID **\_ \_ radice delle classi HKEY** \\  . In caso contrario, vengono usate **\_ le classi HKEY \_ radice** \\ **sconosciuta** .
-   L'estensione del nome file è registrata in **HKEY \_ classi \_ radice** \\ **SystemFileAssociations** \\ *. FileExtension* sottochiave.
-   Nella tabella seguente sono riportati i ProgID speciali. 

    | ProgID speciale                                    | Descrizione                   |
    |---------------------------------------------------|-------------------------------|
    | **HKEY \_ \_radice classi** \\ * *\** _                   | Tutti i file (non cartelle)       |
    | _ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects** | File e cartelle di file system |
    | **HKEY \_ Directory \_ radice classi** \\             | Cartelle del file System           |
    | **HKEY \_ Cartella \_ radice classi** \\                | Contenitori della shell              |

    

     

### <a name="shell-data-source-association-arrays"></a>Matrici di associazioni di origini dati della shell

Nell'elenco seguente sono riportate alcune delle matrici di associazioni dell'archivio dati della shell che possono essere utilizzate per gli scopi descritti in questo argomento:

-   **HKEY \_ \_radice classi** \\ * *\** _
-   _ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects**
-   **HKEY \_ \_Radice delle classi** \\ **Kind.Document**
-   **HKEY \_ Risultati \_ radice classi** \\ 
-   **HKEY \_ Classi \_ radice** \\ **SystemFileAssociations** \\ **. docx**
-   **HKEY \_ \_Radice delle classi** \\ **Word.Document. 12**

Le matrici di associazioni delle origini dati della shell che possono essere usate per DBFolder (un archivio dati della shell che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query) sono le seguenti:

-   Unità
-   Rete
-   RegItems
-   Esempi:
    -   ContentView
    -   Verbi

Altre matrici di associazioni comuni includono cartella e stampanti.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](nse-implement.md).

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

[Tipi percepiti](fa-perceivedtypes.md)
</dt> </dl>

 

 
