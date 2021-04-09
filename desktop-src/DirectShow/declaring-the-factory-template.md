---
description: Dichiarazione del modello Factory
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Dichiarazione del modello Factory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123693"
---
# <a name="declaring-the-factory-template"></a>Dichiarazione del modello Factory

Il passaggio successivo consiste nel dichiarare il modello factory per il filtro. Un modello di Factory è una classe C++ che contiene informazioni per la class factory. Nella DLL dichiarare una matrice globale di oggetti [**CFactoryTemplate**](cfactorytemplate.md) , uno per ogni filtro o componente COM della dll. La matrice deve essere denominata *g \_ templates*. Per ulteriori informazioni sui modelli Factory, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).

Il membro del **\_ \_ filtro pAMovieSetup m** del modello Factory è un puntatore alla struttura [**del \_ filtro AMOVIESETUP**](amoviesetup-filter.md) descritta in precedenza. L'esempio seguente illustra un modello Factory, usando la struttura specificata nell'esempio precedente:


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Se non è stata dichiarata alcuna informazione sul filtro, il **\_ \_ filtro m PAMoveSetup** può essere **null**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare i filtri DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



