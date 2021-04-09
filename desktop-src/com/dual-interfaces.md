---
title: Interfacce duali (COM)
description: Interfacce doppie
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047472"
---
# <a name="dual-interfaces"></a>Interfacce doppie

L'automazione OLE consente a un oggetto di esporre un set di metodi in due modi: tramite l'interfaccia **IDispatch** e tramite l'associazione OLE vtable diretta. **IDispatch** è usato dalla maggior parte degli strumenti attualmente disponibili e offre supporto per l'associazione tardiva a proprietà e metodi.

L'associazione VTable offre prestazioni molto più elevate poiché questo metodo viene chiamato direttamente anziché tramite **IDispatch:: Invoke**. **IDispatch** offre supporto con associazione tardiva, in cui l'associazione vtable diretta offre un miglioramento significativo delle prestazioni. entrambe le tecniche sono utili e importanti in scenari diversi. Etichettando un'interfaccia come \[ [**duale**](/windows/desktop/Midl/dual) \] nella libreria dei tipi, un'interfaccia di automazione OLE può essere usata tramite **IDispatch** oppure può essere associata direttamente a. I contenitori possono quindi scegliere la tecnica più appropriata. Il supporto per le interfacce duali è fortemente consigliato sia per i controlli che per i contenitori.

 

 