---
description: Passaggio 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Passaggio 10. Supporto della registrazione COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68efdeda754d5f7b728138a26a6bc9f4b782918f8c4b5140fd2457bcee6012f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652151"
---
# <a name="step-10-support-com-registration"></a>Passaggio 10. Supporto della registrazione COM

L'ultima attività rimanente è supportare la registrazione COM, in modo che il frame delle proprietà possa creare nuove istanze della pagina delle proprietà. Aggiungere [**un'altra voce CFactoryTemplate**](cfactorytemplate.md) alla matrice *globale g \_ Templates,* usata per registrare tutti gli oggetti COM nella DLL. Non includere informazioni di configurazione del filtro per la pagina delle proprietà.


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



Se si dichiara *g \_ cTemplates* come illustrato nel codice seguente, ha automaticamente il valore corretto in base alle dimensioni della matrice:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Aggiungere anche un metodo statico `CreateInstance` alla classe della pagina delle proprietà. È possibile assegnare al metodo il nome desiderato, ma la firma deve corrispondere a quella illustrata nell'esempio seguente:


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



Per testare la pagina delle proprietà, registrare la DLL e quindi caricare il filtro in GraphEdit. Fare clic con il pulsante destro del mouse sul filtro e **scegliere Proprietà filtro**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà Filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Come creare una DLL DirectShow filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 



