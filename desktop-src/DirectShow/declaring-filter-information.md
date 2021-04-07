---
description: Dichiarazione delle informazioni sul filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Dichiarazione delle informazioni sul filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747410"
---
# <a name="declaring-filter-information"></a>Dichiarazione delle informazioni sul filtro

Il primo passaggio consiste nel dichiarare le informazioni del filtro, se necessario. DirectShow definisce le strutture seguenti per la descrizione di filtri, pin e tipi di supporto:



| Struttura                                               | Descrizione             |
|---------------------------------------------------------|-------------------------|
| [**\_filtro AMOVIESETUP**](amoviesetup-filter.md)       | Descrive un filtro.     |
| [**\_pin AMOVIESETUP**](amoviesetup-pin.md)             | Descrive un PIN.        |
| [**\_MEDIATYPE AMOVIESETUP**](amoviesetup-mediatype.md) | Descrive un tipo di supporto. |



 

Queste strutture sono annidate. La struttura del **\_ filtro AMOVEIESETUP** include un puntatore a una matrice di strutture **AMOVIESETUP \_ pin** e ognuna di esse dispone di un puntatore a una matrice di strutture **AMOVEIESETUP \_ MEDIATYPE** . Insieme, queste strutture forniscono informazioni sufficienti per l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) per individuare un filtro. Non sono una descrizione completa di un filtro. Se, ad esempio, il filtro crea più istanze dello stesso pin, è necessario dichiarare solo una struttura di [**\_ pin AMOVIESETUP**](amoviesetup-pin.md) per tale pin. Inoltre, non è necessario un filtro per supportare ogni combinazione di tipi di supporto registrato; non è necessario per registrare tutti i tipi di supporto supportati.

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

[Come registrare i filtri DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



