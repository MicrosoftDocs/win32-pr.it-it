---
title: Container-Specific interfacce private
description: Container-Specific interfacce private
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a426ae67d3722406ca6c1428d46d0bc3b4a937a1bcdd105de6f376bbe53a5ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550635"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific interfacce private

Alcuni contenitori forniscono interfacce private specifiche del contenitore per funzionalità aggiuntive o prestazioni migliorate. I controlli che si basano su tali interfacce specifiche del contenitore devono, se possibile, funzionare senza le interfacce specifiche del contenitore presenti in modo che funzioni in contenitori diversi. Ad esempio, Visual Basic interfacce private che forniscono funzionalità di formattazione delle stringhe ai controlli. Se un controllo usa queste interfacce di formattazione private, dovrebbe essere in grado di eseguire con il supporto della formattazione predefinito se queste interfacce non sono disponibili. Se il controllo può funzionare senza le interfacce private, deve eseguire le azioni appropriate (ad esempio avvisare l'utente di funzionalità ridotte) ma continuare a funzionare. Se non si tratta di un'opzione, è necessario registrare una categoria di componenti in modo che solo i contenitori che supportano questa funzionalità possano ospitare questi controlli.

 

 




