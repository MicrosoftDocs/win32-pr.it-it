---
title: Proprietà e metodi di navigazione degli oggetti
description: I client passano da un oggetto all'altro usando metodi quali IAccessible accNavigate e IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955367"
---
# <a name="object-navigation-properties-and-methods"></a>Proprietà e metodi di navigazione degli oggetti

I client *passano* da un oggetto all'altro usando metodi quali [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Questi metodi consentono ai client di recuperare un ID figlio o l'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un altro oggetto. La navigazione consente ai client di esplorare il modo in cui gli oggetti sono correlati tra loro. Si noti che la navigazione verso un altro oggetto non modifica la selezione o lo stato attivo.

L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornisce proprietà e metodi che supportano i tipi di navigazione seguenti:

-   [Navigazione gerarchica](hierarchical-navigation.md)
-   [Navigazione spaziale e logica](spatial-and-logical-navigation.md)
-   [Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)

 

 




