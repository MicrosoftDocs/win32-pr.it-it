---
description: Passaggio 3.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Passaggio 3. Supporta QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317223"
---
# <a name="step-3-support-queryinterface"></a>Passaggio 3. Supporta QueryInterface

Per esporre le nuove interfacce del filtro ai client, eseguire le operazioni seguenti:

-   Includere la macro [**Declare \_ IUnknown**](declare-iunknown.md) nella sezione public Declaration del filtro:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Eseguire l'override di [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare la IID delle due interfacce:
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

    

Successivo: [passaggio 4. Creare la pagina delle proprietà](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



