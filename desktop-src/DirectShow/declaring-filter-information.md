---
description: Dichiarazione di informazioni sui filtri
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Dichiarazione di informazioni sui filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953200"
---
# <a name="declaring-filter-information"></a>Dichiarazione di informazioni sui filtri

Il primo passaggio consiste nel dichiarare le informazioni sul filtro, se necessario. DirectShow definisce le strutture seguenti per descrivere filtri, segnaposto e tipi di supporti:



| Struttura                                               | Descrizione             |
|---------------------------------------------------------|-------------------------|
| [**FILTRO \_ AMOVIESETUP**](amoviesetup-filter.md)       | Descrive un filtro.     |
| [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md)             | Descrive un segnaposto.        |
| [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) | Descrive un tipo di supporto. |



 

Queste strutture sono annidate. La **struttura AMOVEIESETUP \_ FILTER** include un puntatore a una matrice di strutture **\_ PIN AMOVIESETUP** e ognuna di queste ha un puntatore a una matrice di **strutture AMOVEIESETUP \_ MEDIATYPE.** Nel loro insieme, queste strutture forniscono informazioni sufficienti per [**l'interfaccia IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) per individuare un filtro. Non sono una descrizione completa di un filtro. Ad esempio, se il filtro crea più istanze dello stesso pin, è necessario dichiarare una sola struttura DI [**\_ PIN AMOVIESETUP**](amoviesetup-pin.md) per tale pin. Inoltre, non è necessario un filtro per supportare ogni combinazione di tipi di supporti registrati. né è necessario per registrare ogni tipo di supporto supportato.

Dichiarare le strutture di configurazione come variabili globali all'interno della DLL. L'esempio seguente mostra un filtro con un pin di output:


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



Il nome del filtro viene dichiarato come variabile globale statica, perché verrà usato di nuovo altrove.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare DirectShow filtri](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



