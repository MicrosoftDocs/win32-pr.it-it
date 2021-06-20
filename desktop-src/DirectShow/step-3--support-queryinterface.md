---
description: Esporre le nuove interfacce di un filtro ai client come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Passaggio 3. Supporto di QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410024"
---
# <a name="step-3-support-queryinterface"></a>Passaggio 3. Supporto di QueryInterface

Per esporre le nuove interfacce del filtro ai client, eseguire le operazioni seguenti:

-   Includere la macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) nella sezione della dichiarazione pubblica del filtro:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Eseguire [**l'override di CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare la presenza degli ID delle due interfacce:
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

Passaggio [4. Creare la pagina delle proprietà](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



