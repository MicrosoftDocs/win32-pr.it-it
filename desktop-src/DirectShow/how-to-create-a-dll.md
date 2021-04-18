---
description: Come creare una DLL di filtro DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Come creare una DLL di filtro DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303728"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Come creare una DLL di filtro DirectShow

Questo articolo descrive come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow. Questo articolo è una continuazione di [come implementare IUnknown](how-to-implement-iunknown.md), che descrive come implementare l'interfaccia **IUnknown** derivando il componente dalla classe base [**CUnknown**](cunknown.md) .

Questo articolo include le sezioni seguenti.

-   [Class factory e modelli di Factory](class-factories-and-factory-templates.md)
-   [Matrice modello Factory](factory-template-array.md)
-   [Funzioni DLL](dll-functions.md)

Per la registrazione di un filtro DirectShow (in contrapposizione a un oggetto COM generico) sono necessari alcuni passaggi aggiuntivi che non sono trattati in questo articolo. Per informazioni sulla registrazione dei filtri, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



