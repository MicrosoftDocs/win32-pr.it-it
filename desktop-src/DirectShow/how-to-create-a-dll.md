---
description: Come creare una DLL DirectShow filtro
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Come creare una DLL DirectShow filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443f8aff88cf73198ed7c417da77f6febf33e18806efba5431e18117ddd2c32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079011"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Come creare una DLL DirectShow filtro

Questo articolo descrive come implementare un componente come libreria a collegamento dinamico (DLL) in Microsoft DirectShow. Questo articolo è una continuazione di Come implementare [IUnknown](how-to-implement-iunknown.md), che descrive come implementare **l'interfaccia IUnknown** derivando il componente dalla classe di base [**CUnknown.**](cunknown.md)

Questo articolo include le sezioni seguenti.

-   [Class Factory e modelli factory](class-factories-and-factory-templates.md)
-   [Factory Template Array](factory-template-array.md)
-   [Funzioni DLL](dll-functions.md)

La registrazione di DirectShow filtro (anziché un oggetto COM generico) richiede alcuni passaggi aggiuntivi non trattati in questo articolo. Per informazioni sulla registrazione dei filtri, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



