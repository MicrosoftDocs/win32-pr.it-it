---
description: Set di proprietà
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Set di proprietà (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401179"
---
# <a name="property-sets-directshow"></a>Set di proprietà (DirectShow)

Microsoft DirectShow usa i set di proprietà per supportare i servizi estesi offerti dall'hardware e i relativi driver e filtri associati. I fornitori di hardware e filtri possono definire nuove funzionalità come proprietà, disporli in set di proprietà e pubblicare la specifica per questi set di proprietà. Lo sviluppatore di applicazioni può utilizzare i metodi dell'interfaccia [**IKsPropertySet**](ikspropertyset.md) per determinare se un driver o un filtro supporta un determinato set di proprietà e recuperare o impostare tali proprietà.

Tutti i metodi esposti da **IKsPropertySet** richiedono un **GUID** che identifichi il set di proprietà (parametro *GuidPropSet* ) e un **valore DWORD** che identifica la proprietà all'interno del set di proprietà (parametro *dwPropID* ). Il parametro *dwPropID* è in genere un membro di un tipo di dati enumerato.

Le singole proprietà possono avere dati associati specificati nel parametro *pPropData* nei metodi [**IKsPropertySet:: set**](ikspropertyset-set.md) e [**IKsPropertySet:: Get**](ikspropertyset-get.md) . In questi metodi, i dati della proprietà sono tipizzati come puntatore a `void` . Il tipo di dati e il significato dei dati vengono specificati nella definizione del set di proprietà.

Le sezioni seguenti forniscono informazioni sui set di proprietà supportati in DirectShow:

-   [**Set di proprietà di protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Set di proprietà di DVD karaoke**](dvd-karaoke-property-set.md)
-   [**Set di proprietà della sottoimmagine DVD**](dvd-subpicture-property-set.md)
-   [Set di proprietà di trasporto dispositivo esterno](external-device-transport-property-set.md)
-   [Set di proprietà di avanzamento frame](frame-stepping-property-set.md)
-   [Imposta la proprietà pin](pin-property-set.md)
-   [**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)

 

 



