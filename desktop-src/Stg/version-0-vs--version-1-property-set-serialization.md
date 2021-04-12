---
title: Serializzazione del set di proprietà
description: Sono disponibili due versioni del formato di serializzazione del set di proprietà.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c635728e169cdddb20437323a49a18496b3459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223947"
---
# <a name="property-set-serialization"></a>Serializzazione del set di proprietà

Sono disponibili due versioni del formato di serializzazione del set di proprietà. La specifica originale descrive la versione 0 del formato. Per ulteriori informazioni, vedere [format version](format-version.md) . La versione 1 estende la versione originale. Tutti i set di proprietà della versione 0 sono validi come set di proprietà versione 1. Il campo della **versione del formato** nell'intestazione di un set di proprietà serializzate indica la versione.

Gli elementi seguenti identificano le differenze tra i formati di serializzazione del set di proprietà versione 0 e 1.

-   Supporto per nuovi valori **VarType** . Per ulteriori informazioni sui valori **VarType** e su come utilizzarli, vedere l'argomento [tipi di dati e strutture di IDispatch]( /previous-versions/ms221600(v=vs.100)) e la struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

    I valori **VarType** seguenti non sono supportati nei set di proprietà della versione 0, ma sono supportati nella versione 1:

    VT \_ I1

    VT \_ vettore \| VT \_ I1

    \_int VT

    \_uint VT

    \_decimale VT

    È inoltre possibile serializzare SafeArrays in un set di proprietà. La presenza di un SafeArray è indicata dal bit di \_ matrice VT combinato, tramite un'operazione **or** , con gli elementi della matrice nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Ad esempio, un SafeArray di interi con segno a 4 byte ha un tipo di VT di \_ matrice VT \| \_ i4.

    I tipi di elemento seguenti sono validi per un SafeArray in un set di proprietà serializzate:



|             |          |             |           |
|-------------|----------|-------------|-----------|
| VT \_ I1      | \_Ui1 VT  | \_I2 VT      | \_UI2 VT   |
| VT \_ I4      | \_UI4 VT  | \_int VT     | \_uint VT  |
| \_R4 VT      | VT \_ R8   | \_CY VT      | \_Data VT  |
| \_BSTR VT    | \_bool VT | \_decimale VT | \_errore VT |
| \_variante VT |          |             |           |



 

Quando \_ viene specificato il tipo di dati Variant VT, il SAFEARRAY stesso include le strutture [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . I tipi per questi elementi devono provenire dall'elenco precedente, ad eccezione del fatto che non possono contenere tipi varianti VT annidati \_ .

Si noti che le implementazioni di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) devono essere in grado di eseguire il ripristino normalmente restituendo un errore quando viene rilevato un nuovo tipo. ad esempio, i tipi VARENUM.

-   Nomi proprietà con distinzione tra maiuscole e minuscole. I nomi delle proprietà, ad esempio quelli specificati nel metodo [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) , non fanno distinzione tra maiuscole e minuscole nei set di proprietà della versione 0. Nei set di proprietà della versione 1 i nomi di proprietà possono fare distinzione tra maiuscole e minuscole a seconda del valore della nuova proprietà Behavior.

    La proprietà Behavior è [ID di proprietà 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) con un tipo di \_ UI4 VT. Se viene impostato il bit più basso di questo valore, i nomi dei set di proprietà fanno distinzione tra maiuscole e minuscole. Impostare il flag PROPSETFLAG maiuscole \_ \_ /minuscole nel parametro *GrfFlags* del metodo [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) per specificare un set di proprietà con distinzione tra maiuscole e minuscole.

-   Nomi di proprietà Long. I nomi di proprietà per i set di proprietà della versione 0 devono essere minori o uguali a 256 caratteri, incluso il carattere di terminazione della stringa, per i set di proprietà nella tabella codici Unicode. Se non è presente nella tabella codici Unicode, è necessario che siano inferiori a 256 byte. I set di proprietà della versione 1, d'altra parte, possono avere nomi di proprietà di lunghezza illimitata, anche se sono comunque limitati dal limite complessivo delle dimensioni del set di proprietà di 256 kilobyte (KB).

Per impostazione predefinita, è consigliabile che le implementazioni di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creino e gestiscano i set di proprietà della versione 0. Se successivamente un chiamante richiede una funzionalità specifica del formato versione 1, solo la versione del set di proprietà deve essere aggiornata. Se, ad esempio, viene scritta una proprietà di tipo VT \_ Array o se viene scritto un nome di proprietà Long, l'implementazione deve aggiornare il formato del set di proprietà alla versione 1. Un'eccezione a questa linea guida si verifica se il \_ valore di enumerazione con distinzione tra maiuscole e \_ minuscole PROPSETFLAG viene specificato nella chiamata a [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). In questo caso, è necessario creare il set di proprietà come set di proprietà della versione 1.

 

 