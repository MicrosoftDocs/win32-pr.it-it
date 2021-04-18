---
description: Passaggio 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Passaggio 10. Supporto della registrazione COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314406"
---
# <a name="step-10-support-com-registration"></a>Passaggio 10. Supporto della registrazione COM

L'ultima attività rimanente è supportare la registrazione COM, in modo che il frame della proprietà possa creare nuove istanze della pagina delle proprietà. Aggiungere un'altra voce [**CFactoryTemplate**](cfactorytemplate.md) alla matrice *di \_ modelli g* globale, che viene usata per registrare tutti gli oggetti com nella dll. Non includere le informazioni di configurazione del filtro per la pagina delle proprietà.


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



Se si dichiara *g \_ cTemplates* come illustrato nel codice seguente, il valore corretto verrà automaticamente in base alle dimensioni della matrice:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Aggiungere inoltre un metodo statico `CreateInstance` alla classe della pagina delle proprietà. È possibile denominare il metodo in qualsiasi modo desiderato, ma la firma deve corrispondere a quella illustrata nell'esempio seguente:


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



Per eseguire il test della pagina delle proprietà, registrare la DLL e quindi caricare il filtro in GraphEdit. Fare clic con il pulsante destro del mouse sul filtro e selezionare **Proprietà filtro**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Come creare una DLL di filtro DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 



