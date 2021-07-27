---
title: Serializzazione del set di proprietà
description: Esistono due versioni del formato di serializzazione del set di proprietà.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d8dfc1c51a6d33d6eb6f9c22b513a9a5397c87
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436290"
---
# <a name="property-set-serialization"></a>Serializzazione del set di proprietà

Esistono due versioni del formato di serializzazione del set di proprietà. La specifica originale descrive la versione 0 del formato. Per [altre informazioni, vedere](format-version.md) Versione del formato. La versione 1 estende la versione originale. Tutti i set di proprietà versione 0 sono validi come set di proprietà della versione 1. Il **campo Versione formato** nell'intestazione di un set di proprietà serializzate indica la versione.

Gli elementi seguenti identificano le differenze tra i formati di serializzazione del set di proprietà versione 0 e versione 1.

-   Supporto per i **nuovi valori VARTYPE.** Per altre informazioni sui **valori VARTYPE** e su come usarli, vedere l'argomento [IDispatch Data Types and Structures e]( /previous-versions/ms221600(v=vs.100)) la [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

    I valori **VARTYPE** seguenti non sono supportati nei set di proprietà della versione 0, ma sono supportati nella versione 1:

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    È anche possibile serializzare SafeArrays in un set di proprietà. La presenza di un oggetto SafeArray è indicata dal bit VT_ARRAY combinato, usando un'operazione **OR,** con gli elementi della matrice nel membro **vt** della [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Ad esempio, un oggetto SafeArray di interi con segno a 4 byte ha un tipo di VT_ARRAY \| VT_I4.

    I tipi di elemento seguenti sono validi per safearray in un set di proprietà serializzate:

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Quando viene VT_VARIANT tipo di dati, indica che SafeArray contiene strutture [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) I tipi per questi elementi devono essere dell'elenco precedente, ma non possono contenere tipi VT_VARIANT annidati.
    
    Si noti che le implementazioni [**di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) devono essere in grado di eseguire correttamente il ripristino restituisce un errore quando viene rilevato un nuovo tipo. ad esempio i tipi VARENUM.

-   Nomi di proprietà con distinzione tra maiuscole e minuscole. I nomi delle proprietà, ad esempio quelli specificati nel metodo [**IPropertyStorage::WritePropertyNames,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) non fa distinzione tra maiuscole e minuscole nei set di proprietà della versione 0. Nei set di proprietà versione 1 i nomi delle proprietà possono fare distinzione tra maiuscole e minuscole a seconda del valore della nuova proprietà Behavior.

    La proprietà Behavior è [l'ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) con un tipo di VT_UI4. Se il bit più basso di questo valore è impostato, per i nomi dei set di proprietà viene fatto distinzione tra maiuscole e minuscole. Impostare il flag PROPSETFLAG_CASE_SENSITIVE flag nel *parametro grfFlags* del metodo [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) per specificare un set di proprietà con distinzione tra maiuscole e minuscole.

-   Nomi di proprietà lunghi. I nomi delle proprietà per i set di proprietà versione 0 devono essere minori o uguali a 256 caratteri, incluso il carattere di terminazione della stringa, per i set di proprietà nella tabella codici Unicode. Se non sono presenti nella tabella codici Unicode, devono essere inferiori a 256 byte. I set di proprietà versione 1, d'altra parte, possono avere nomi di proprietà di lunghezza illimitata, anche se sono ancora limitati dal limite complessivo delle dimensioni del set di proprietà di 256 kilobyte (KB).

È consigliabile che le implementazioni di [**IPropertyStorage creino**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e mantengano set di proprietà versione 0 per impostazione predefinita. Se un chiamante successivamente richiede una funzionalità specifica del formato versione 1, solo la versione del set di proprietà deve essere aggiornata. Ad esempio, se viene scritta una proprietà di tipo VT_ARRAY o se viene scritto un nome di proprietà long, l'implementazione deve aggiornare il formato del set di proprietà alla versione 1. Un'eccezione a questa linea guida si verifica se il PROPSETFLAG_CASE_SENSITIVE di enumerazione viene specificato nella chiamata a [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). In questo caso, il set di proprietà deve essere creato come set di proprietà versione 1.

 

 